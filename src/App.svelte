<script>
	import NavBar from './lib/NavBar.svelte';
	import Icon from './assets/Icon.png';
  import { Router } from "@roxi/routify";
  import routes from "../.routify/routes.default.js";
  import { Button, Offcanvas } from 'sveltestrap';
  
  let open = false;
  const toggle = () => (open = !open);
</script>

<svelte:head>
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.0/dist/css/bootstrap.min.css">
</svelte:head>

<!-- Remove the rest of this file's contents after the router: -->
<NavBar />
<Router {routes} />


<style>


</style>
