<script lang="ts">
	import Navbar from '../lib/Navbar.svelte';
	import user from '../lib/Navbar.svelte';
	import { auth, googleProvider } from '../firebase/firebase';
	function login() {
		auth.signInWithPopup(googleProvider);
	}
</script>
<Navbar/>
<section class="container h-screen flex mx-auto px-4">
	<div class="flex flex-col justify-center align-middle w-full text-center">
		<h1 class="text-7xl font-extrabold text-slate-200">Conversations made simple.</h1>
		<h2 class="py-3 text-2xl antialiased text-slate-400 ">
			Lorem ipsum dolor sit amet consectetur adipisicing elit. Cumque, eaque?
		</h2>
		{#if user}
			<a
				href="/app"
				class="mx-auto my-2 rounded-xl px-5 py-2 text-white border transition-all ease-in hover:bg-white hover:text-gray-800 duration-200"
				>Open App</a
			>
		{:else}
			<a
				href="/"
				class="mx-auto my-2 rounded-xl px-5 py-2 text-white border transition-all ease-in hover:bg-white hover:text-gray-800 duration-200"
				on:click={login}>Sign Up</a
			>
		{/if}
	</div>
</section>
<section>
	<article>
		<h1>test</h1>
	</article>
</section>
