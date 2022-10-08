<!-- <script>
  import svelteLogo from './assets/svelte.svg'
  import Counter from './lib/Counter.svelte'
</script>

<main>
  <div>
    <a href="https://vitejs.dev" target="_blank"> 
      <img src="/vite.svg" class="logo" alt="Vite Logo" />
    </a>
    <a href="https://svelte.dev" target="_blank"> 
      <img src={svelteLogo} class="logo svelte" alt="Svelte Logo" />
    </a>
  </div>
  <h1>Vite + Svelte</h1>

  <div class="card">
    <Counter />
  </div>

  <p>
    Check out <a href="https://github.com/sveltejs/kit#readme" target="_blank">SvelteKit</a>, the official Svelte app framework powered by Vite!
  </p>

  <p class="read-the-docs">
    Click on the Vite and Svelte logos to learn more
  </p>
</main>

<style>
  .logo {
    height: 6em;
    padding: 1.5em;
    will-change: filter;
  }
  .logo:hover {
    filter: drop-shadow(0 0 2em #646cffaa);
  }
  .logo.svelte:hover {
    filter: drop-shadow(0 0 2em #ff3e00aa);
  }
  .read-the-docs {
    color: #888;
  }
</style> -->

<script>
	import router from 'page';
	import Home from './pages/Home.svelte';
	import About from './pages/About.svelte';
	import Product from './pages/Product.svelte';
  import Brand from './pages/Brand.svelte';


	// import Project from './pages/Projects.svelte';

	const baseUrl = '';
	
	let page, subNav = '', uri, params, getParams;

	router(`${baseUrl}home`, () => (page = Home, uri = '/home', subNav = ''));
  router(`${baseUrl}about`, () => (page = About, uri = '/about', subNav = ''));
  router(`${baseUrl}product`, () => (page = Product, uri = '/product', subNav = ''));
  router(`${baseUrl}brand`, () => (page = Brand, uri = '/brand', subNav = ''));

	router(`${baseUrl}`, () => (page = Home, uri = '/home', subNav = ''));
	// router(`${baseUrl}projects/`,() => (page = Project, uri = '/projects', subNav = ''));
	// router (
	// 	`${baseUrl}projects/detail/:id`,
	// 	(ctx, next) => {
	// 		params = ctx.params;
	// 		next(); 
	// 	}, 
	// 	() => (page = Project, uri = '/projects', subNav = 'detail')
	// );

	router.start();
</script>

<svelte:component this={page} subNav={subNav} {baseUrl} params={params} />
