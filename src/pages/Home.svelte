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
        Heloo..
        <Splide aria-label="My Favorite Images">
            <SplideSlide>
            
              <img src="http://majuselaras.com/cms/assets/uploads/slider/1539156620.png" class="image-banner" alt="Image 1"/>
            </SplideSlide>
            <SplideSlide>
              <img src="{svelteLogo}" class="image-banner" alt="Image 2"/>
            </SplideSlide>
        </Splide>
       
        <div class="row pt-2">
            <div class="col-6 pe-1">
                <img src="{svelteLogo}" class="image-banner" alt="Image 1"/>
            </div>
            <div class="col-6 ps-1">
                <img src="{svelteLogo}" class="image-banner" alt="Image 1"/>
            </div>
        </div>
    </div>
    <div class="">
        <img src="{sectionimg1}" class="image-section" alt="Image 1"/>
    </div>

    <Splide
    options={ {
        // type   : 'loop',
        drag   : 'free',
        perPage: 2,
        trimSpace:true,
        padding: { right: 40 },
        arrows:false,
        pagination:false,
        

    } }
    >
        <SplideSlide>
            <div class="m-1">
            <div class="card" style="">
                <div class="" style="height: 100%;box-sizing: border-box;">
                <div style="overflow: visible;border: 1px solid transparent;     text-decoration: none;
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
                    <div style="width: 100%;padding-top: 100%;      position: relative;">
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
        </SplideSlide>
        <SplideSlide>
            <div class="m-1">
            <div class="card" style="">
                <div class="" style="height: 100%;box-sizing: border-box;">
                <div style="overflow: visible;border: 1px solid transparent;     text-decoration: none;
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
                    <div style="width: 100%;padding-top: 100%;      position: relative;">
                        <img width="invalid-value" height="invalid-value" alt="Maybelline Superstay Matte Ink Liquid Matte Lipstick Make Up [ Tahan Lama Hingga 16 Jam ]" class="Vz6gJ3 edy5hG" style="object-fit: contain" src="http://majuselaras.com/cms/assets/uploads/product/1595226491.jpeg">
                    </div>
                    </div>
                    <div class="W3bJfG">
                    <div class="qUEEG4">
                        <div class="hPc1Pf">
                            <div class="vc0PvV AxYdVM">Air Sampler Impinger MS-001-GS AC/DC</div>
                        </div>
                    <!-- <div class="bVKmWS"><div class="_1PWkR nt-medium nt-foot _3nkRL" style="color: rgb(246, 145, 19);"><svg class="_2DRZW _2xFcL" viewBox="-0.5 -0.5 4 16"><path d="M4 0h-3q-1 0 -1 1a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3q0 1 1 1h3" stroke-width="1" transform="" stroke="currentColor" fill="#f69113"></path></svg><div class="_1FKkT _3Ao0A" style="color: white; background-color: rgb(246, 145, 19);">Diskon 7%</div><svg class="_2DRZW _2xFcL" viewBox="-0.5 -0.5 4 16"><path d="M4 0h-3q-1 0 -1 1a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3q0 1 1 1h3" stroke-width="1" transform="rotate(180) translate(-3 -15)" stroke="currentColor" fill="#f69113"></path></svg></div></div></div> -->
                    <!-- <div class="imdVqB _2fuFWg"><div class="WSVId4 fepoRf"><span class="Fea6JM">Rp</span><span class="j0vBz2">94.900</span></div><div class="upl8wJ _82UoSS">10RB+ Terjual</div></div> -->
            
                    </div>
                </div>
                </div>
            </div>
            </div>
        </SplideSlide>
        <SplideSlide>
            <div class="m-1">
            <div class="card" style="">
                <div class="" style="height: 100%;box-sizing: border-box;">
                <div style="overflow: visible;border: 1px solid transparent;     text-decoration: none;
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
                    <div style="width: 100%;padding-top: 100%;      position: relative;">
                        <img width="invalid-value" height="invalid-value" alt="Maybelline Superstay Matte Ink Liquid Matte Lipstick Make Up [ Tahan Lama Hingga 16 Jam ]" class="Vz6gJ3 edy5hG" style="object-fit: contain" src="http://majuselaras.com/cms/assets/uploads/product/1643879792.jpeg">
                    </div>
                    </div>
                    <div class="W3bJfG">
                    <div class="qUEEG4">
                        <div class="hPc1Pf">
                            <div class="vc0PvV AxYdVM">Isokinetic Sampling System MS 002 IDS Plus</div>
                        </div>
                    <!-- <div class="bVKmWS"><div class="_1PWkR nt-medium nt-foot _3nkRL" style="color: rgb(246, 145, 19);"><svg class="_2DRZW _2xFcL" viewBox="-0.5 -0.5 4 16"><path d="M4 0h-3q-1 0 -1 1a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3q0 1 1 1h3" stroke-width="1" transform="" stroke="currentColor" fill="#f69113"></path></svg><div class="_1FKkT _3Ao0A" style="color: white; background-color: rgb(246, 145, 19);">Diskon 7%</div><svg class="_2DRZW _2xFcL" viewBox="-0.5 -0.5 4 16"><path d="M4 0h-3q-1 0 -1 1a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3q0 1 1 1h3" stroke-width="1" transform="rotate(180) translate(-3 -15)" stroke="currentColor" fill="#f69113"></path></svg></div></div></div> -->
                    <!-- <div class="imdVqB _2fuFWg"><div class="WSVId4 fepoRf"><span class="Fea6JM">Rp</span><span class="j0vBz2">94.900</span></div><div class="upl8wJ _82UoSS">10RB+ Terjual</div></div> -->
            
                    </div>
                </div>
                </div>
            </div>
            </div>
        </SplideSlide>
        
        <SplideSlide>
            <div class="m-1">
            <div class="card" style="">
                <div class="" style="height: 100%;box-sizing: border-box;">
                <div style="overflow: visible;border: 1px solid transparent;     text-decoration: none;
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
                    <div style="width: 100%;padding-top: 100%;      position: relative;">
                        <img width="invalid-value" height="invalid-value" alt="Maybelline Superstay Matte Ink Liquid Matte Lipstick Make Up [ Tahan Lama Hingga 16 Jam ]" class="Vz6gJ3 edy5hG" style="object-fit: contain" src="http://majuselaras.com/cms/assets/uploads/product/1595237837.jpeg">
                    </div>
                    </div>
                    <div class="W3bJfG">
                    <div class="qUEEG4">
                        <div class="hPc1Pf">
                            <div class="vc0PvV AxYdVM">Isokinetic Sampling System Method 17</div>
                        </div>
                    <!-- <div class="bVKmWS"><div class="_1PWkR nt-medium nt-foot _3nkRL" style="color: rgb(246, 145, 19);"><svg class="_2DRZW _2xFcL" viewBox="-0.5 -0.5 4 16"><path d="M4 0h-3q-1 0 -1 1a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3q0 1 1 1h3" stroke-width="1" transform="" stroke="currentColor" fill="#f69113"></path></svg><div class="_1FKkT _3Ao0A" style="color: white; background-color: rgb(246, 145, 19);">Diskon 7%</div><svg class="_2DRZW _2xFcL" viewBox="-0.5 -0.5 4 16"><path d="M4 0h-3q-1 0 -1 1a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3q0 1 1 1h3" stroke-width="1" transform="rotate(180) translate(-3 -15)" stroke="currentColor" fill="#f69113"></path></svg></div></div></div> -->
                    <!-- <div class="imdVqB _2fuFWg"><div class="WSVId4 fepoRf"><span class="Fea6JM">Rp</span><span class="j0vBz2">94.900</span></div><div class="upl8wJ _82UoSS">10RB+ Terjual</div></div> -->
            
                    </div>
                </div>
                </div>
            </div>
            </div>
        </SplideSlide>
        <SplideSlide>
            <div class="m-1">
            <div class="card" style="">
                <div class="" style="height: 100%;box-sizing: border-box;">
                <div style="overflow: visible;border: 1px solid transparent;     text-decoration: none;
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
                    <div style="width: 100%;padding-top: 100%;      position: relative;">
                        <img width="invalid-value" height="invalid-value" alt="Maybelline Superstay Matte Ink Liquid Matte Lipstick Make Up [ Tahan Lama Hingga 16 Jam ]" class="Vz6gJ3 edy5hG" style="object-fit: contain" src="http://majuselaras.com/cms/assets/uploads/product/1641799718.jpg">
                    </div>
                    </div>
                    <div class="W3bJfG">
                    <div class="qUEEG4">
                        <div class="hPc1Pf">
                            <div class="vc0PvV AxYdVM">KEG-500</div>
                        </div>
                    <!-- <div class="bVKmWS"><div class="_1PWkR nt-medium nt-foot _3nkRL" style="color: rgb(246, 145, 19);"><svg class="_2DRZW _2xFcL" viewBox="-0.5 -0.5 4 16"><path d="M4 0h-3q-1 0 -1 1a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3q0 1 1 1h3" stroke-width="1" transform="" stroke="currentColor" fill="#f69113"></path></svg><div class="_1FKkT _3Ao0A" style="color: white; background-color: rgb(246, 145, 19);">Diskon 7%</div><svg class="_2DRZW _2xFcL" viewBox="-0.5 -0.5 4 16"><path d="M4 0h-3q-1 0 -1 1a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3q0 1 1 1h3" stroke-width="1" transform="rotate(180) translate(-3 -15)" stroke="currentColor" fill="#f69113"></path></svg></div></div></div> -->
                    <!-- <div class="imdVqB _2fuFWg"><div class="WSVId4 fepoRf"><span class="Fea6JM">Rp</span><span class="j0vBz2">94.900</span></div><div class="upl8wJ _82UoSS">10RB+ Terjual</div></div> -->
            
                    </div>
                </div>
                </div>
            </div>
            </div>
        </SplideSlide>
        <SplideSlide>
            <div class="m-1">
            <div class="card" style="">
                <div class="" style="height: 100%;box-sizing: border-box;">
                <div style="overflow: visible;border: 1px solid transparent;     text-decoration: none;
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
                    <div style="width: 100%;padding-top: 100%;      position: relative;">
                        <img width="invalid-value" height="invalid-value" alt="Maybelline Superstay Matte Ink Liquid Matte Lipstick Make Up [ Tahan Lama Hingga 16 Jam ]" class="Vz6gJ3 edy5hG" style="object-fit: contain" src="http://majuselaras.com/cms/assets/uploads/product/1595230706.jpeg">
                    </div>
                    </div>
                    <div class="W3bJfG">
                    <div class="qUEEG4">
                        <div class="hPc1Pf">
                            <div class="vc0PvV AxYdVM">Water Sampler MS 001 WS</div>
                        </div>
                    <!-- <div class="bVKmWS"><div class="_1PWkR nt-medium nt-foot _3nkRL" style="color: rgb(246, 145, 19);"><svg class="_2DRZW _2xFcL" viewBox="-0.5 -0.5 4 16"><path d="M4 0h-3q-1 0 -1 1a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3q0 1 1 1h3" stroke-width="1" transform="" stroke="currentColor" fill="#f69113"></path></svg><div class="_1FKkT _3Ao0A" style="color: white; background-color: rgb(246, 145, 19);">Diskon 7%</div><svg class="_2DRZW _2xFcL" viewBox="-0.5 -0.5 4 16"><path d="M4 0h-3q-1 0 -1 1a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3q0 1 1 1h3" stroke-width="1" transform="rotate(180) translate(-3 -15)" stroke="currentColor" fill="#f69113"></path></svg></div></div></div> -->
                    <!-- <div class="imdVqB _2fuFWg"><div class="WSVId4 fepoRf"><span class="Fea6JM">Rp</span><span class="j0vBz2">94.900</span></div><div class="upl8wJ _82UoSS">10RB+ Terjual</div></div> -->
            
                    </div>
                </div>
                </div>
            </div>
            </div>
        </SplideSlide>
        
    </Splide>


    <div class="">
        <img src="{sectionimg1}" class="image-section" alt="Image 1"/>
    </div>

    <Splide
    options={ {
        // type   : 'loop',
        drag   : 'free',
        perPage: 3,
        trimSpace:true,
        padding: { right: 40 },
        arrows:false,
        pagination:false,
        

    } }
    >
        <SplideSlide>
            <div class="m-2 d-flex justify-content-center">
                <img src="http://majuselaras.com/cms/assets/uploads/principal/1538424351.png" class="image-banner" alt="Image 1"/>
            </div>
        </SplideSlide>

        <SplideSlide>
            <div class="m-2">
                <img src="http://majuselaras.com/cms/assets/uploads/principal/1538424495.png" class="image-banner" alt="Image 1"/>
            </div>
        </SplideSlide>
        <SplideSlide>
            <div class="m-2">
                <img src="http://majuselaras.com/cms/assets/uploads/principal/1538424452.png" class="image-banner" alt="Image 1"/>
            </div>
        </SplideSlide>
        <SplideSlide>
            <div class="m-2">
                <img src="http://majuselaras.com/cms/assets/uploads/principal/1641797434.png" class="image-banner" alt="Image 1"/>
            </div>
        </SplideSlide>
    </Splide>



    <Splide
    options={ {
        // type   : 'loop',
        drag   : 'free',
        perPage: 2,
        trimSpace:true,
        padding: { right: 40 },
        arrows:false,
        pagination:false,
        

    } }
    >
        <SplideSlide>
            <div class="m-1">
            <div class="card" style="">
                <div class="" style="height: 100%;box-sizing: border-box;">
                  <div style="overflow: visible;border: 1px solid transparent;     text-decoration: none;
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
                      <div style="width: 100%;padding-top: 100%;      position: relative;">
                        <img width="invalid-value" height="invalid-value" alt="Maybelline Superstay Matte Ink Liquid Matte Lipstick Make Up [ Tahan Lama Hingga 16 Jam ]" class="Vz6gJ3 edy5hG" style="object-fit: contain" src="http://majuselaras.com/cms/assets/uploads/product/1538639245.jpg">
                      </div>
                    </div>
                    <div class="W3bJfG">
                      <div class="qUEEG4"><div class="hPc1Pf"><div class="vc0PvV AxYdVM">Maybelline Superstay Matte Ink Liquid Matte Lipstick Make Up [ Tahan Lama Hingga 16 Jam ]</div></div><div class="bVKmWS"><div class="_1PWkR nt-medium nt-foot _3nkRL" style="color: rgb(246, 145, 19);"><svg class="_2DRZW _2xFcL" viewBox="-0.5 -0.5 4 16"><path d="M4 0h-3q-1 0 -1 1a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3q0 1 1 1h3" stroke-width="1" transform="" stroke="currentColor" fill="#f69113"></path></svg><div class="_1FKkT _3Ao0A" style="color: white; background-color: rgb(246, 145, 19);">Diskon 7%</div><svg class="_2DRZW _2xFcL" viewBox="-0.5 -0.5 4 16"><path d="M4 0h-3q-1 0 -1 1a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3v0.333a1.2 1.5 0 0 1 0 3q0 1 1 1h3" stroke-width="1" transform="rotate(180) translate(-3 -15)" stroke="currentColor" fill="#f69113"></path></svg></div></div></div>
                      <div class="imdVqB _2fuFWg"><div class="WSVId4 fepoRf"><span class="Fea6JM">Rp</span><span class="j0vBz2">94.900</span></div><div class="upl8wJ _82UoSS">10RB+ Terjual</div></div>
            
                    </div>
                  </div>
                </div>
              </div>
            </div>
        </SplideSlide>
        <SplideSlide>
            <div class="m-1">
                <div class="card" style="border-radius: 9px;">
                    <img src="{svelteLogo}" class="card-img-top"  alt="Image 1"/>
                    <div class="card-body" style="padding:8px;">
                        <h6 class="card-title">Air Sampler Impinger  MS-003-GS</h6>
                        <!-- <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p> -->
                    </div>
                </div>
            </div>
        </SplideSlide>
        <SplideSlide>
            <div class="m-1">
                <div class="card" style="border-radius: 9px;">
                    <img src="{svelteLogo}" class="card-img-top"  alt="Image 1"/>
                    <div class="card-body" style="padding:8px;">
                        <h6 class="card-title">Air Sampler Impinger  MS-003-GS</h6>
                        <!-- <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p> -->
                    </div>
                </div>
            </div>
        </SplideSlide>
        <SplideSlide>
            <div class="m-1">
                <div class="card" style="border-radius: 9px;">
                    <img src="{svelteLogo}" class="card-img-top"  alt="Image 1"/>
                    <div class="card-body" style="padding:8px;">
                        <h6 class="card-title">Air Sampler Impinger  MS-003-GS</h6>
                        <!-- <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p> -->
                    </div>
                </div>
            </div>
        </SplideSlide>
        <SplideSlide>
            <div class="m-1">
                <div class="card" style="border-radius: 9px;">
                    <img src="https://images.tokopedia.net/img/cache/300-square/VqbcmM/2021/10/21/cc30db51-e3a2-40ad-91e5-efdb5a8ce430.jpg.webp?ect=4g" class="card-img-top"  alt="Image 1"/>
                    <div class="card-body" style="padding:8px;">
                        <h6 class="card-title">Air Sampler Impinger  MS-003-GS</h6>
                        <!-- <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p> -->
                    </div>
                </div>
            </div>
        </SplideSlide>
        <SplideSlide>
            <div class="m-1">
                <img src="{svelteLogo}" class="image-banner" alt="Image 1"/>
            </div>
        </SplideSlide>
        <SplideSlide>
            <div class="m-1">
                <img src="{svelteLogo}" class="image-banner" alt="Image 1"/>
            </div>
        </SplideSlide>
        <SplideSlide>
            <div class="m-1">
                <img src="{svelteLogo}" class="image-banner" alt="Image 1"/>
            </div>
        </SplideSlide>
        <SplideSlide>
            <div class="m-1">
                <img src="{svelteLogo}" class="image-banner" alt="Image 1"/>
            </div>
        </SplideSlide>
        <SplideSlide>
            <div class="m-1">
                <img src="{svelteLogo}" class="image-banner" alt="Image 1"/>
            </div>
        </SplideSlide>
    </Splide>

   