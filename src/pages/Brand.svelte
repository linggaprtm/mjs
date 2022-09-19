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


    .menu-category{
        text-align: left;
        overflow: auto hidden;
        white-space: nowrap;
        transition: all 0.5s ease 0s;
        display: flex;
        -webkit-box-pack: justify;
        /* justify-content: center; */
        -webkit-box-align: center;
        align-items: center;
        padding-top: 10px;
        padding-bottom: 10px;
    }

    .menu-category a {
        text-decoration: none;
        padding-top: 9px;
        padding-bottom: 9px;
        opacity: 0.3;
        line-height: 20px;
        font-weight: 500;
        letter-spacing: 1px;
        margin-left: 20px;
        margin-right: 20px;
        color: #121212;
        transition: color 200ms ease 0s;
        -webkit-font-smoothing: antialiased;
    }

    .menu-subcategory{
        text-align: left;
        overflow: auto hidden;
        white-space: nowrap;
        transition: all 0.5s ease 0s;
        display: flex;
        -webkit-box-pack: justify;
        /* justify-content: center; */
        -webkit-box-align: center;
        align-items: center;
        padding-top: 10px;
        padding-bottom: 10px;
        background-color: blanchedalmond;
    }

    .menu-subcategory a {
        text-decoration: none;
        padding-top: 9px;
        padding-bottom: 9px;
        opacity: 0.3;
        line-height: 20px;
        font-weight: 500;
        letter-spacing: 1px;
        margin-left: 20px;
        margin-right: 20px;
        color: #121212;
        transition: color 200ms ease 0s;
        -webkit-font-smoothing: antialiased;
    }
    
  

</style>

    <!-- <div class="menu-category">
        <a href="#">All Brands</a>
        <a href="#">MS Instrument</a>
        <a href="#">Air Metric</a>
        <a href="#">Solinst</a>
        <a href="#">CETCII Critical Instrument</a>
        <a href="#">General Eqiupment</a>
        <a href="#">HTI</a>
        <a href="#">Environmental Devices Corporation</a>
        <a href="#">Sauerman</a>
        <a href="#">TSI Quest</a>
        <a href="#">Kimo (Sauermann Group)</a>
        <a href="#">Koeng</a>
        <a href="#">Eutech Instruments</a>
        <a href="#">Staplex</a>
        <a href="#">Shinagawa</a>
        <a href="#">Hach</a>
        <a href="#">Extech</a>
        <a href="#">TISCH Environtmental</a>
        <a href="#">Peak Instruments</a>
    </div> -->

    <div class="menu-subcategory">
        <a href="#">All Brands</a>
        <a href="#">MS Instrument</a>
        <a href="#">Air Metric</a>
        <a href="#">Solinst</a>
        <a href="#">CETCII Critical Instrument</a>
        <a href="#">General Eqiupment</a>
        <a href="#">HTI</a>
        <a href="#">Environmental Devices Corporation</a>
        <a href="#">Sauerman</a>
        <a href="#">TSI Quest</a>
        <a href="#">Kimo (Sauermann Group)</a>
        <a href="#">Koeng</a>
        <a href="#">Eutech Instruments</a>
        <a href="#">Staplex</a>
        <a href="#">Shinagawa</a>
        <a href="#">Hach</a>
        <a href="#">Extech</a>
        <a href="#">TISCH Environtmental</a>
        <a href="#">Peak Instruments</a>
    </div>

<div class="m-2"></div>
<div class="container">
    <div class="row">
        <div class="col-6 p-1">
            <div class="card" >
                <div class="" style="height: 100%;box-sizing: border-box;">
                    <div style="overflow: visible;border: 1px solid transparent;text-decoration: none;
                    color: rgba(0,0,0,.87);
                    display: block;
                    box-shadow: 0 0.0625rem 0.125rem 0 rgb(0 0 0 / 10%);
                    border-radius: 0.125rem;
                    overflow: hidden;
                    display: flex;
                    flex-direction: column;
                    background: #fff;
                    position: relative;
                    overflow: visible;
                    cursor: pointer;
                    -webkit-user-select: none;
                    -moz-user-select: none;
                    user-select: none;
                    padding: 0;
                    transition: transform .1s cubic-bezier(.4,0,.6,1),box-shadow .1s cubic-bezier(.4,0,.6,1);">
                        <div style="pointer-events: none;">
                            <div style="width: 100%;padding-top: 100%;position: relative;">
                                <img width="invalid-value" height="invalid-value" alt="Maybelline Superstay Matte Ink Liquid Matte Lipstick Make Up [ Tahan Lama Hingga 16 Jam ]" class="Vz6gJ3 edy5hG" style="object-fit: contain" src="http://majuselaras.com/cms/assets/uploads/product/1595228159.jpeg">
                            </div>
                        </div>
                        <div class="W3bJfG">
                            <div class="qUEEG4">
                                <div class="hPc1Pf">
                                    <div class="card-title vc0PvV AxYdVM">Air Sampler Impinger  MS-003-GS</div>
                                </div>
                        <!-- <div class="bVKmWS"><div class="_1PWkR nt-medium nt-foot _3nkRL" style="color: rgb(246, 145, 19);"><svg class="_2DRZW _2xFcL" viewBox="-0.5 -0.5 4 16"><path d="M4 0h-3q-1 0 -1 1a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3q0 1 1 1h3" stroke-width="1" transform="" stroke="currentColor" fill="#f69113"></path></svg><div class="_1FKkT _3Ao0A" style="color: white; background-color: rgb(246, 145, 19);">Diskon 7%</div><svg class="_2DRZW _2xFcL" viewBox="-0.5 -0.5 4 16"><path d="M4 0h-3q-1 0 -1 1a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3q0 1 1 1h3" stroke-width="1" transform="rotate(180) translate(-3 -15)" stroke="currentColor" fill="#f69113"></path></svg></div></div></div> -->
                        <!-- <div class="imdVqB _2fuFWg"><div class="WSVId4 fepoRf"><span class="Fea6JM">Rp</span><span class="j0vBz2">94.900</span></div><div class="upl8wJ _82UoSS">10RB+ Terjual</div></div> -->
                
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="col-6 p-1">
            <div class="card" >
                <div class="" style="height: 100%;box-sizing: border-box;">
                    <div style="overflow: visible;border: 1px solid transparent;text-decoration: none;
                    color: rgba(0,0,0,.87);
                    display: block;
                    box-shadow: 0 0.0625rem 0.125rem 0 rgb(0 0 0 / 10%);
                    border-radius: 0.125rem;
                    overflow: hidden;
                    display: flex;
                    flex-direction: column;
                    background: #fff;
                    position: relative;
                    overflow: visible;
                    cursor: pointer;
                    -webkit-user-select: none;
                    -moz-user-select: none;
                    user-select: none;
                    padding: 0;
                    transition: transform .1s cubic-bezier(.4,0,.6,1),box-shadow .1s cubic-bezier(.4,0,.6,1);">
                        <div style="pointer-events: none;">
                            <div style="width: 100%;padding-top: 100%;position: relative;">
                                <img width="invalid-value" height="invalid-value" alt="Maybelline Superstay Matte Ink Liquid Matte Lipstick Make Up [ Tahan Lama Hingga 16 Jam ]" class="Vz6gJ3 edy5hG" style="object-fit: contain" src="http://majuselaras.com/cms/assets/uploads/product/1595228159.jpeg">
                            </div>
                        </div>
                        <div class="W3bJfG">
                            <div class="qUEEG4">
                                <div class="hPc1Pf">
                                    <div class="card-title vc0PvV AxYdVM">Air Sampler Impinger  MS-003-GS</div>
                                </div>
                        <!-- <div class="bVKmWS"><div class="_1PWkR nt-medium nt-foot _3nkRL" style="color: rgb(246, 145, 19);"><svg class="_2DRZW _2xFcL" viewBox="-0.5 -0.5 4 16"><path d="M4 0h-3q-1 0 -1 1a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3q0 1 1 1h3" stroke-width="1" transform="" stroke="currentColor" fill="#f69113"></path></svg><div class="_1FKkT _3Ao0A" style="color: white; background-color: rgb(246, 145, 19);">Diskon 7%</div><svg class="_2DRZW _2xFcL" viewBox="-0.5 -0.5 4 16"><path d="M4 0h-3q-1 0 -1 1a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3q0 1 1 1h3" stroke-width="1" transform="rotate(180) translate(-3 -15)" stroke="currentColor" fill="#f69113"></path></svg></div></div></div> -->
                        <!-- <div class="imdVqB _2fuFWg"><div class="WSVId4 fepoRf"><span class="Fea6JM">Rp</span><span class="j0vBz2">94.900</span></div><div class="upl8wJ _82UoSS">10RB+ Terjual</div></div> -->
                
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="col-6 p-1">
            <div class="card" >
                <div class="" style="height: 100%;box-sizing: border-box;">
                    <div style="overflow: visible;border: 1px solid transparent;text-decoration: none;
                    color: rgba(0,0,0,.87);
                    display: block;
                    box-shadow: 0 0.0625rem 0.125rem 0 rgb(0 0 0 / 10%);
                    border-radius: 0.125rem;
                    overflow: hidden;
                    display: flex;
                    flex-direction: column;
                    background: #fff;
                    position: relative;
                    overflow: visible;
                    cursor: pointer;
                    -webkit-user-select: none;
                    -moz-user-select: none;
                    user-select: none;
                    padding: 0;
                    transition: transform .1s cubic-bezier(.4,0,.6,1),box-shadow .1s cubic-bezier(.4,0,.6,1);">
                        <div style="pointer-events: none;">
                            <div style="width: 100%;padding-top: 100%;position: relative;">
                                <img width="invalid-value" height="invalid-value" alt="Maybelline Superstay Matte Ink Liquid Matte Lipstick Make Up [ Tahan Lama Hingga 16 Jam ]" class="Vz6gJ3 edy5hG" style="object-fit: contain" src="http://majuselaras.com/cms/assets/uploads/product/1595228159.jpeg">
                            </div>
                        </div>
                        <div class="W3bJfG">
                            <div class="qUEEG4">
                                <div class="hPc1Pf">
                                    <div class="card-title vc0PvV AxYdVM">Air Sampler Impinger  MS-003-GS</div>
                                </div>
                        <!-- <div class="bVKmWS"><div class="_1PWkR nt-medium nt-foot _3nkRL" style="color: rgb(246, 145, 19);"><svg class="_2DRZW _2xFcL" viewBox="-0.5 -0.5 4 16"><path d="M4 0h-3q-1 0 -1 1a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3q0 1 1 1h3" stroke-width="1" transform="" stroke="currentColor" fill="#f69113"></path></svg><div class="_1FKkT _3Ao0A" style="color: white; background-color: rgb(246, 145, 19);">Diskon 7%</div><svg class="_2DRZW _2xFcL" viewBox="-0.5 -0.5 4 16"><path d="M4 0h-3q-1 0 -1 1a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3q0 1 1 1h3" stroke-width="1" transform="rotate(180) translate(-3 -15)" stroke="currentColor" fill="#f69113"></path></svg></div></div></div> -->
                        <!-- <div class="imdVqB _2fuFWg"><div class="WSVId4 fepoRf"><span class="Fea6JM">Rp</span><span class="j0vBz2">94.900</span></div><div class="upl8wJ _82UoSS">10RB+ Terjual</div></div> -->
                
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="col-6 p-1">
            <div class="card" >
                <div class="" style="height: 100%;box-sizing: border-box;">
                    <div style="overflow: visible;border: 1px solid transparent;text-decoration: none;
                    color: rgba(0,0,0,.87);
                    display: block;
                    box-shadow: 0 0.0625rem 0.125rem 0 rgb(0 0 0 / 10%);
                    border-radius: 0.125rem;
                    overflow: hidden;
                    display: flex;
                    flex-direction: column;
                    background: #fff;
                    position: relative;
                    overflow: visible;
                    cursor: pointer;
                    -webkit-user-select: none;
                    -moz-user-select: none;
                    user-select: none;
                    padding: 0;
                    transition: transform .1s cubic-bezier(.4,0,.6,1),box-shadow .1s cubic-bezier(.4,0,.6,1);">
                        <div style="pointer-events: none;">
                            <div style="width: 100%;padding-top: 100%;position: relative;">
                                <img width="invalid-value" height="invalid-value" alt="Maybelline Superstay Matte Ink Liquid Matte Lipstick Make Up [ Tahan Lama Hingga 16 Jam ]" class="Vz6gJ3 edy5hG" style="object-fit: contain" src="http://majuselaras.com/cms/assets/uploads/product/1595228159.jpeg">
                            </div>
                        </div>
                        <div class="W3bJfG">
                            <div class="qUEEG4">
                                <div class="hPc1Pf">
                                    <div class="card-title vc0PvV AxYdVM">Air Sampler Impinger  MS-003-GS</div>
                                </div>
                        <!-- <div class="bVKmWS"><div class="_1PWkR nt-medium nt-foot _3nkRL" style="color: rgb(246, 145, 19);"><svg class="_2DRZW _2xFcL" viewBox="-0.5 -0.5 4 16"><path d="M4 0h-3q-1 0 -1 1a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3q0 1 1 1h3" stroke-width="1" transform="" stroke="currentColor" fill="#f69113"></path></svg><div class="_1FKkT _3Ao0A" style="color: white; background-color: rgb(246, 145, 19);">Diskon 7%</div><svg class="_2DRZW _2xFcL" viewBox="-0.5 -0.5 4 16"><path d="M4 0h-3q-1 0 -1 1a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3q0 1 1 1h3" stroke-width="1" transform="rotate(180) translate(-3 -15)" stroke="currentColor" fill="#f69113"></path></svg></div></div></div> -->
                        <!-- <div class="imdVqB _2fuFWg"><div class="WSVId4 fepoRf"><span class="Fea6JM">Rp</span><span class="j0vBz2">94.900</span></div><div class="upl8wJ _82UoSS">10RB+ Terjual</div></div> -->
                
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="col-6 p-1">
            <div class="card" >
                <div class="" style="height: 100%;box-sizing: border-box;">
                    <div style="overflow: visible;border: 1px solid transparent;text-decoration: none;
                    color: rgba(0,0,0,.87);
                    display: block;
                    box-shadow: 0 0.0625rem 0.125rem 0 rgb(0 0 0 / 10%);
                    border-radius: 0.125rem;
                    overflow: hidden;
                    display: flex;
                    flex-direction: column;
                    background: #fff;
                    position: relative;
                    overflow: visible;
                    cursor: pointer;
                    -webkit-user-select: none;
                    -moz-user-select: none;
                    user-select: none;
                    padding: 0;
                    transition: transform .1s cubic-bezier(.4,0,.6,1),box-shadow .1s cubic-bezier(.4,0,.6,1);">
                        <div style="pointer-events: none;">
                            <div style="width: 100%;padding-top: 100%;position: relative;">
                                <img width="invalid-value" height="invalid-value" alt="Maybelline Superstay Matte Ink Liquid Matte Lipstick Make Up [ Tahan Lama Hingga 16 Jam ]" class="Vz6gJ3 edy5hG" style="object-fit: contain" src="http://majuselaras.com/cms/assets/uploads/product/1595228159.jpeg">
                            </div>
                        </div>
                        <div class="W3bJfG">
                            <div class="qUEEG4">
                                <div class="hPc1Pf">
                                    <div class="card-title vc0PvV AxYdVM">Air Sampler Impinger  MS-003-GS</div>
                                </div>
                        <!-- <div class="bVKmWS"><div class="_1PWkR nt-medium nt-foot _3nkRL" style="color: rgb(246, 145, 19);"><svg class="_2DRZW _2xFcL" viewBox="-0.5 -0.5 4 16"><path d="M4 0h-3q-1 0 -1 1a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3q0 1 1 1h3" stroke-width="1" transform="" stroke="currentColor" fill="#f69113"></path></svg><div class="_1FKkT _3Ao0A" style="color: white; background-color: rgb(246, 145, 19);">Diskon 7%</div><svg class="_2DRZW _2xFcL" viewBox="-0.5 -0.5 4 16"><path d="M4 0h-3q-1 0 -1 1a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3q0 1 1 1h3" stroke-width="1" transform="rotate(180) translate(-3 -15)" stroke="currentColor" fill="#f69113"></path></svg></div></div></div> -->
                        <!-- <div class="imdVqB _2fuFWg"><div class="WSVId4 fepoRf"><span class="Fea6JM">Rp</span><span class="j0vBz2">94.900</span></div><div class="upl8wJ _82UoSS">10RB+ Terjual</div></div> -->
                
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="col-6 p-1">
            <div class="card" >
                <div class="" style="height: 100%;box-sizing: border-box;">
                    <div style="overflow: visible;border: 1px solid transparent;text-decoration: none;
                    color: rgba(0,0,0,.87);
                    display: block;
                    box-shadow: 0 0.0625rem 0.125rem 0 rgb(0 0 0 / 10%);
                    border-radius: 0.125rem;
                    overflow: hidden;
                    display: flex;
                    flex-direction: column;
                    background: #fff;
                    position: relative;
                    overflow: visible;
                    cursor: pointer;
                    -webkit-user-select: none;
                    -moz-user-select: none;
                    user-select: none;
                    padding: 0;
                    transition: transform .1s cubic-bezier(.4,0,.6,1),box-shadow .1s cubic-bezier(.4,0,.6,1);">
                        <div style="pointer-events: none;">
                            <div style="width: 100%;padding-top: 100%;position: relative;">
                                <img width="invalid-value" height="invalid-value" alt="Maybelline Superstay Matte Ink Liquid Matte Lipstick Make Up [ Tahan Lama Hingga 16 Jam ]" class="Vz6gJ3 edy5hG" style="object-fit: contain" src="http://majuselaras.com/cms/assets/uploads/product/1595228159.jpeg">
                            </div>
                        </div>
                        <div class="W3bJfG">
                            <div class="qUEEG4">
                                <div class="hPc1Pf">
                                    <div class="card-title vc0PvV AxYdVM">Air Sampler Impinger  MS-003-GS</div>
                                </div>
                        <!-- <div class="bVKmWS"><div class="_1PWkR nt-medium nt-foot _3nkRL" style="color: rgb(246, 145, 19);"><svg class="_2DRZW _2xFcL" viewBox="-0.5 -0.5 4 16"><path d="M4 0h-3q-1 0 -1 1a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3q0 1 1 1h3" stroke-width="1" transform="" stroke="currentColor" fill="#f69113"></path></svg><div class="_1FKkT _3Ao0A" style="color: white; background-color: rgb(246, 145, 19);">Diskon 7%</div><svg class="_2DRZW _2xFcL" viewBox="-0.5 -0.5 4 16"><path d="M4 0h-3q-1 0 -1 1a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3q0 1 1 1h3" stroke-width="1" transform="rotate(180) translate(-3 -15)" stroke="currentColor" fill="#f69113"></path></svg></div></div></div> -->
                        <!-- <div class="imdVqB _2fuFWg"><div class="WSVId4 fepoRf"><span class="Fea6JM">Rp</span><span class="j0vBz2">94.900</span></div><div class="upl8wJ _82UoSS">10RB+ Terjual</div></div> -->
                
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>


   

