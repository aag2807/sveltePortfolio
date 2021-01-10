<script lang="ts">
	import Router from "svelte-spa-router";

	import { Container } from 'svelte-materialify'
	//component imports
	import Navbar from "./components/Navbar.svelte";
	import Divider from "./utils/Divider.svelte";
	import Footer from "./components/Footer.svelte";

	//Helper imports
	import { routes } from "./routes/routes";
</script>

<style lang="scss">

	main {
		width:100%;
		max-width:100%;
	}
</style>


<main>
	<Navbar />
	<Divider />

	<Container>
		<Router {routes} />
	</Container>
	<Footer />
</main>
