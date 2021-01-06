<script lang="ts">
	import Router from "svelte-spa-router";

	//component imports
	import Navbar from "./components/Navbar.svelte";
	import Divider from "./utils/Divider.svelte";
	import Footer from "./components/Footer.svelte";

	//Helper imports
	import { routes } from "./routes/routes";
</script>

<style lang="scss">
</style>

<svelte:head>
	<link
		href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.0-beta1/dist/css/bootstrap.min.css"
		rel="stylesheet"
		integrity="sha384-giJF6kkoqNQ00vy+HMDP7azOuL0xtbfIcaT9wjKHr8RbDVddVHyTfAAsrekwKmP1"
		crossorigin="anonymous" />
	<script
		src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.0-beta1/dist/js/bootstrap.bundle.min.js"
		integrity="sha384-ygbV9kiqUc6oa4msXn9868pTtWMgiQaeYH7/t7LECLbyPA2x65Kgf80OJFdroafW"
		crossorigin="anonymous">
	</script>
</svelte:head>

<main>
	<Navbar />
	<Divider />

	<div class="container">
		<Router {routes} />
	</div>

	<Footer />
</main>
