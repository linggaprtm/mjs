<script>
    import {onMount} from 'svelte';
    // import Header from '../components/Header.svelte';
    // import Footer from '../components/Footer.svelte';
    // import { storeCategories, storeBanner, storeProjectsHome } from '../data/store.js';
    import { Splide, SplideSlide } from '@splidejs/svelte-splide';
    import svelteLogo from '../assets/images/contoh_banner.webp'
    import sectionimg1 from '../assets/images/section1.png'
    // Default theme
    import '@splidejs/svelte-splide/css';

    export let baseUrl;

   

    
    
    // async function postData(url = '', data = {}) {

    //     let formBody = [];
    //     for (var property in data) {
    //         var encodedKey = encodeURIComponent(property);
    //         var encodedValue = encodeURIComponent(data[property]);
    //         formBody.push(encodedKey + "=" + encodedValue);
    //     }
    //     formBody = formBody.join("&");

    //     // Default options are marked with *
    //     const response = await fetch(url, {
    //         method: 'POST', // *GET, POST, PUT, DELETE, etc.
    //         mode: 'cors', // no-cors, *cors, same-origin
    //         // cache: 'no-cache', // *default, no-cache, reload, force-cache, only-if-cached
    //         // credentials: 'same-origin', // include, *same-origin, omit
    //         headers: {
    //         //  'Accept': 'text/html, */*; q=0.01',
    //         'Content-Type': 'application/json',
    //         'Content-Type': 'application/x-www-form-urlencoded; charset=UTF-8',
    //         'X-Requested-With': 'XMLHttpRequest'
    //         },
    //         redirect: 'follow', // manual, *follow, error
    //         referrerPolicy: 'no-referrer', // no-referrer, *no-referrer-when-downgrade, origin, origin-when-cross-origin, same-origin, strict-origin, strict-origin-when-cross-origin, unsafe-url
    //         body: formBody//JSON.stringify(data) // body data type must match "Content-Type" header
    //     });
    //     return response.json(); // parses JSON response into native JavaScript objects
    // }

    let dataBanner = '';
    // $storeBanner = {};
    //Get Banner
    // async function getBanner() {
    //     const data = {
    //         valid : 1, 
    //     };

    //     await postData(`${baseUrl}api/get-banner`, data)
    //     .then(res => {
    //         if(res.status) {
    //             dataBanner = res;
    //             $storeBanner = res;
    //         }

    //     });
    // }

    let dataCategory = '';
    // $storeCategories = {};
    // //Get Category
    // async function getCategory() {
    //     const data = {
    //         valid : 1, 
    //     };

    //     await postData(`${baseUrl}api/get-category`, data)
    //     .then(res => {
    //         if(res.status) {
    //             dataCategory = res;
    //             $storeCategories = res;
    //         }

    //     });
    // }

    let dataProjects = '';
    // $storeProjectsHome = {};
    // //Get Category
    // async function getProjects() {
    //     const data = {
    //         valid       : 1, 
    //         limit       : '',
    //         offset      : '',
    //         category    : '',
    //         keyword     : ''
    //     };

    //     await postData(`${baseUrl}api/get-project`, data)
    //     .then(res => {
    //         if(res.status) {
    //             dataProjects = res;
    //             $storeProjectsHome = res; 
    //         }

    //     });
    // }

    // onMount(async function () {
    //     await getBanner();
    //     await getCategory();
    //     await getProjects();
    // });
</script>

<style>
    .placeholder-item {
        box-shadow: 0 4px 10px 0 rgba(33, 33, 33, 0.15);
        border-radius: 9px;
        height: 200px;
        position: relative;
        overflow: hidden;
    }
    .placeholder-item::before {
        content: '';
        display: block;
        position: absolute;
        left: -150px;
        top: 0;
        height: 100%;
        width: 150px;
        background: linear-gradient(to right, transparent 0%, #E8E8E8 50%, transparent 100%);
        animation: load 1s cubic-bezier(0.4, 0.0, 0.2, 1) infinite;
    }
    .image-banner{
        /* border: 0.5px solid rgb(229, 231, 233); */
        border-radius: 10px;
        width: 100%;
    }
    .image-section{
        /* border: 0.5px solid rgb(229, 231, 233);
        border-radius: 10px; */
        width: 100%;
    }
    @keyframes load {
        from {
            left: -150px;
        }
        to   {
            left: 100%;
        }
    }

    .n-CE6j img {
      vertical-align: bottom;
    }
  
    .Vz6gJ3 {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: #fff;
    }
  
    .qUEEG4, .W3bJfG {
      flex: 1 0 auto;
      display: flex;
      flex-direction: column;
    }
  
    .W3bJfG {
      padding: 0.3rem;
      overflow: hidden;
      font-weight: 600;
    }
  
    .hPc1Pf {
      flex-grow: 1;
      min-height: 1.75rem;
    }
  
    .AxYdVM.AxYdVM {
      display: inline-block;
      word-wrap: break-word;
      white-space: normal;
      overflow: hidden;
      display: -webkit-box;
      text-overflow: ellipsis;
      -webkit-box-orient: vertical;
      -webkit-line-clamp: 3;
    }
  
    .vc0PvV {
      display: inline;
      font-size: 14px;
      /* line-height: 14px; */
      /* font-size: .75rem; */
    }
    .fepoRf {
      flex: 1 0 auto;
      max-width: 75%;
      color: #ee4d2d;
    }
  
  
    .bVKmWS>div:only-child {
      flex-shrink: 0;
    }
  
    .nt-medium {
      font-family: var(--nt-font-medium-f,-apple-system,'HelveticaNeue-Medium','Helvetica Neue','Roboto','Droid Sans',Arial,sans-serif);
      font-weight: var(--nt-font-medium-w,500);
    }
  
    ._1PWkR {
      box-sizing: border-box;
      display: inline-block;
      height: 1rem;
      min-width: 0;
      position: relative;
      overflow: hidden;
    }
  
  
  
    .bVKmWS {
      display: flex;
      height: 1rem;
      align-items: center;
      overflow: hidden;
      margin-top: 0.25rem;
    }
  
    ._2fuFWg {
      padding: 0.5rem 0 0;
      display: flex;
      height: 1.25rem;
      align-items: center;
      overflow: hidden;
    }
  
  
  
    .WSVId4 {
      display: inline;
      white-space: nowrap;
      text-overflow: ellipsis;
      overflow: hidden;
    }
  
    ._82UoSS._82UoSS {
      color: rgba(0,0,0,.54);
    }
  
    ._82UoSS._82UoSS, .fepoRf {
      overflow: hidden;
      text-overflow: ellipsis;
      white-space: nowrap;
    
    }
  
    .upl8wJ {
      color: rgba(0,0,0,.87);
      line-height: .875rem;
      overflow: hidden;
      white-space: nowrap;
      text-overflow: ellipsis;
    }
    .upl8wJ {
      color: rgba(0,0,0,.87);
      line-height: .875rem;
      overflow: hidden;
      white-space: nowrap;
      text-overflow: ellipsis;
    }
    .Fea6JM, .upl8wJ {
      font-size: .75rem;
    }
  

</style>

    <div class="container">
       
       
       
        <div class="row pt-2">
            <div class="col-12 ">
                <img src="{svelteLogo}" class="image-banner" alt="Image 1"/>
            </div>
            <div class="col-12 ">
               <p>
                Tentang Kami
               </p>
            </div>
        </div>
    </div>
   

   