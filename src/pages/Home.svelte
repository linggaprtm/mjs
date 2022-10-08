<script>
    import {onMount} from 'svelte';
    import Product from './Product.svelte';
    // import Footer from '../components/Footer.svelte';
    // import { storeCategories, storeBanner, storeProjectsHome } from '../data/store.js';
    import { Splide, SplideSlide } from '@splidejs/svelte-splide';
    import svelteLogoMs from '../assets/images/logo-large.jpg';
    import svelteLogo from '../assets/images/contoh_banner.webp';
    import banner1 from '../assets/images/banner1.png';
    import videoimage from '../assets/images/videoimage.png';
    import sectionimg1 from '../assets/images/section1.png';
    import deviderOurCustomer from '../assets/images/our-customer.png';
    import deviderNewProduct from '../assets/images/new-product.png';
    import deviderOurPrincipal from '../assets/images/our-principal.png';


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
<header class="site-header sticky-top" style="background-color:#ffff;">
    <nav class="navbar navbar-expand-lg d-flex flex-column flex-md-row"
      aria-label="Eighth navbar example">
      <div class="container">
        <a class="navbar-brand me-4" href="/">
          <img src="{svelteLogoMs}" class="" style="max-width:130px;" alt="logo"/>
          <!-- <div>hello</div> -->
        </a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarsExample07"
          aria-controls="navbarsExample07" aria-expanded="false" aria-label="Toggle navigation">
          <svg viewBox="0 0 100 100" width="30" height="30" >
            <path class="opened line line1" d="M 20,29.000046 H 80.000231 C 80.000231,29.000046 94.498839,28.817352 94.532987,66.711331 94.543142,77.980673 90.966081,81.670246 85.259173,81.668997 79.552261,81.667751 75.000211,74.999942 75.000211,74.999942 L 25.000021,25.000058" />
            <path class="opened line line2" d="M 20,50 H 80" />
            <path class="opened line line3" d="M 20,70.999954 H 80.000231 C 80.000231,70.999954 94.498839,71.182648 94.532987,33.288669 94.543142,22.019327 90.966081,18.329754 85.259173,18.331003 79.552261,18.332249 75.000211,25.000058 75.000211,25.000058 L 25.000021,74.999942" />
          </svg>
        </button>

        <div class="collapse navbar-collapse" id="navbarsExample07">
          <ul class="navbar-nav me-auto mb-2 mb-lg-0 ">
            <!-- <li class="nav-item dropdown">
              <a class="nav-link dropdown-toggle" href="/product" id="dropdown07" data-bs-toggle="dropdown"
                aria-expanded="false">Products</a>
              <ul class="dropdown-menu" aria-labelledby="dropdown07">
                <li style="border-bottom: 1px solid #ced4da;"><a class="dropdown-item" href="product/fumigant/postoxin-56-tb.html">Fumigant</a></li>
                <li  style="border-bottom: 1px solid #ced4da;"><a class="dropdown-item" href="product/insecticide/insecticide.html">Insecticide</a></li>
                <li  style="border-bottom: 1px solid #ced4da;">
                  <a class="dropdown-item" href="product/safety/5600.html">Safety</a>
                </li>
                <li style="border-bottom: 1px solid #ced4da;">
                  <a class="dropdown-item" href="product/tools/pt-test-kit.html">Tools</a>
                </li>
              </ul>
            </li> -->
            <li class="nav-item">
              <a class="nav-link" href="/product">Product </a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="/brand">Brands </a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="/about">About </a>
            </li>
            <!-- <li class="nav-item">
              <a class="nav-link" href="value.html">Corporate Values </a>
            </li> -->
            <!-- <li class="nav-item dropdown">
              <a class="nav-link dropdown-toggle" href="#" id="dropdown08" data-bs-toggle="dropdown"
                aria-expanded="false">Newsletter</a>
              <ul class="dropdown-menu" aria-labelledby="dropdown08">
                <li><a class="dropdown-item" href="newsletter/product-palsu.html">Produk Palsu</a></li>
                <li>
                  <a class="dropdown-item" href="newsletter/variant-palsu.html">Varian Phostoxin Amerika Palsu</a>
                </li>
                <li><a class="dropdown-item" href="newsletter/perbedaan-product-palsu.html">Perbedaan Product Palsu</a></li>
              </ul>
            </li> -->
            <li class="nav-item">
              <a class="nav-link" href="/contact">Contact </a>
            </li>
          </ul>
          <!-- <form class="d-flex" name="searchProductForm" action="" >
            <input class="form-control field-search" name="fsearch" type="text" placeholder="Search" aria-label="Search" />
            <div id="search-button" class="btn text-white btn-search" >
              <svg height="19" viewBox="0 0 19 19" width="19" class="search-svg-icon"><g fill-rule="evenodd" stroke="none" stroke-width="1"><g transform="translate(-1016 -32)"><g><g transform="translate(405 21)"><g transform="translate(611 11)"><path d="m8 16c4.418278 0 8-3.581722 8-8s-3.581722-8-8-8-8 3.581722-8 8 3.581722 8 8 8zm0-2c-3.3137085 0-6-2.6862915-6-6s2.6862915-6 6-6 6 2.6862915 6 6-2.6862915 6-6 6z"></path><path d="m12.2972351 13.7114222 4.9799555 4.919354c.3929077.3881263 1.0260608.3842503 1.4141871-.0086574.3881263-.3929076.3842503-1.0260607-.0086574-1.414187l-4.9799554-4.919354c-.3929077-.3881263-1.0260608-.3842503-1.4141871.0086573-.3881263.3929077-.3842503 1.0260608.0086573 1.4141871z"></path></g></g></g></g></g></svg>  
            </div>
          </form> -->
        </div>
      </div>
    </nav>
  </header>

    <div class="container mt-2">
        <Splide aria-label="My Favorite Images">
            <SplideSlide>
              <img src="{banner1}" class="image-banner" alt="Image 1"/>
            </SplideSlide>
            <SplideSlide>
              <img src="http://majuselaras.com/cms/assets/uploads/slider/1539156620.png" class="image-banner" alt="Image 1"/>
            </SplideSlide>
            <SplideSlide>
              <img src="{svelteLogo}" class="image-banner" alt="Image 2"/>
            </SplideSlide>
        </Splide>
       
        <div class="row pt-2">
            <div class="col-6 pe-1">
                <img src="{videoimage}" class="image-banner" alt="Image 1"/>
            </div>
            <div class="col-6 ps-1">
                <img src="{videoimage}" class="image-banner" alt="Image 1"/>
            </div>
        </div>
    </div>

    
    <div class="mt-2">
        <img src="{deviderNewProduct}" class="image-section" alt="Image 1"/>
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
                    <div style="width: 100%;padding-top: 100%;      position: relative;">
                        <img width="invalid-value" height="invalid-value" alt="Maybelline Superstay Matte Ink Liquid Matte Lipstick Make Up [ Tahan Lama Hingga 16 Jam ]" class="Vz6gJ3 edy5hG" style="object-fit: contain" src="http://majuselaras.com/cms/assets/uploads/product/1643879792.jpeg">
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
                      <div style="width: 100%;padding-top: 100%;position: relative;">
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
        <img src="{deviderOurCustomer}" class="image-section" alt="Image 1"/>
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
            <div class="m-2  d-flex justify-content-center">
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

    <div class="">
        <img src="{deviderOurPrincipal}" class="image-section" alt="Image 1"/>
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
            <div class="m-2  d-flex justify-content-center">
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



    

   