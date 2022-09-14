<script>
    import {onMount} from 'svelte';
    import Header from '../components/Header.svelte';
    import Footer from '../components/Footer.svelte';
    import { storeCategories } from '../data/store.js';

	import DetailProject from '../projects/DetailProjects.svelte';
	import ListProject from '../projects/ListProjects.svelte';

    export let subNav, baseUrl, params;

    async function postData(url = '', data = {}) {
        let formBody = [];
        for (var property in data) {
            var encodedKey = encodeURIComponent(property);
            var encodedValue = encodeURIComponent(data[property]);
            formBody.push(encodedKey + "=" + encodedValue);
        }
        formBody = formBody.join("&");

        // Default options are marked with *
        const response = await fetch(url, {
            method: 'POST', // *GET, POST, PUT, DELETE, etc.
            mode: 'cors', // no-cors, *cors, same-origin
            // cache: 'no-cache', // *default, no-cache, reload, force-cache, only-if-cached
            // credentials: 'same-origin', // include, *same-origin, omit
            headers: {
            //  'Accept': 'text/html, */*; q=0.01',
            'Content-Type': 'application/json',
            'Content-Type': 'application/x-www-form-urlencoded; charset=UTF-8',
            'X-Requested-With': 'XMLHttpRequest'
            },
            redirect: 'follow', // manual, *follow, error
            referrerPolicy: 'no-referrer', // no-referrer, *no-referrer-when-downgrade, origin, origin-when-cross-origin, same-origin, strict-origin, strict-origin-when-cross-origin, unsafe-url
            body: formBody//JSON.stringify(data) // body data type must match "Content-Type" header
        });
        return response.json(); // parses JSON response into native JavaScript objects
    }

    //parameter get query string values
    const getParams = new URLSearchParams(window.location.search);

    let dataBanner = '';
    //Get Banner
    async function getBanner() {
        const data = {
            valid : 1, 
        };

        await postData(`${baseUrl}api/get-banner`, data)
        .then(res => {
            if(res.status) {
                dataBanner = res;
            }

        });
    }

    let dataCategory = '';
    //Get Category
    async function getCategory() {
        const data = {
            valid : 1, 
        }; 

        await postData(`${baseUrl}api/get-category`, data)
        .then(res => {
            if(res.status) {
                dataCategory = res;
                $storeCategories = dataCategory;
            }

        });
    }

    let dataProjects = '';
    //Get Category
    async function getProjects() {
        const data = {
            valid       : 1, 
            limit       : '',
            offset      : '',
            category    : (getParams.get('category') !== null)?getParams.get('category'):'',
            keyword     : (getParams.get('search') !== null)?getParams.get('search'):''
        };

        await postData(`${baseUrl}api/get-project`, data)
        .then(res => {
            if(res.status) {
                dataProjects = res;
            }

        });
    }

    onMount(async function () {
        await getBanner();
        await getCategory();
        await getProjects();
    });
</script>

<style>
.text11-content{
    padding: 30px;
    background-color: var(--bg-color);
    box-shadow: rgb(1 1 1 / 5%) 1px 1px 5px 0px;
    border-radius: var(--border-radius-full);
}

</style>
    <svelte:component this={Header} baseUrl={baseUrl}/>
    
    <div class="w3l-homeblock2 py-5">
        <div class="container py-lg-5 py-md-4">
            <!-- block -->
            <div class="row">
                {#if subNav === 'detail'}
                    <DetailProject {baseUrl} {params}/>
                {:else}
                    <ListProject {baseUrl}/>	         
                {/if}
              
            </div>
        </div>
    </div>
  
    <svelte:component this={Footer} baseUrl={baseUrl}/>
 