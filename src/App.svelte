<script>
	import {Router, Link, Route} from "svelte-routing";
	import Home from "./views/Home.svelte"
	import About from "./views/About.svelte"
	import Perfil from "./views/Perfil.svelte"
	import Login from "./views/Login.svelte"
	import Navbar from "./components/Navbar.svelte"
</script>

<div class="text-center pt-4">
	<h1>Hola Router</h1>
	<Router>

		<Navbar />

		<Route path="/">
			<Home></Home>
		</Route>

		<Route path="/about">
			<About></About>
		</Route>

		<Route path="/perfil">
			<Perfil></Perfil>
		</Route>

		<Route path="/login">
			<Login></Login>
		</Route>

	</Router>
</div>



<style>
	h1{
		color:coral;
	}
</style>