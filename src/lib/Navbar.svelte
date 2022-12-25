<script lang="ts">
	import { auth, googleProvider } from '../firebase/firebase';
	import { authState } from 'rxfire/auth';
	import type { Auth } from 'firebase/auth';

	export let user: any;

	const unsubscribe = authState(auth).subscribe((usr) => (user = usr));

	export function login() {
		auth.signInWithPopup(googleProvider);
	}

	function logout() {
		auth.signOut();
	}
</script>

<nav
	class="container py-3 mx-auto absolute inset-x-0 top-0 flex flex-row justify-between px-4 font-bold text-lg"
>
	<div class="flex">
		<a href="" class="rounded-lg px-3 py-2 text-slate-200 text-2xl"><strong>chattr.</strong></a>
	</div>
	<div class="flex gap-3">
		<a
			href="#"
			class="rounded-lg px-3 py-2 text-slate-200 hover:text-sky-400 transition ease-linear">Home</a
		>
		<a
			href="#"
			class="rounded-lg px-3 py-2 text-slate-200 hover:text-sky-400 transition ease-linear">About</a
		>
		<a
			href="#"
			class="rounded-lg px-3 py-2 text-slate-200 hover:text-sky-400 transition ease-linear"
			>Testimonials</a
		>
		{#if user}
		<a
			href="/app"
			class="rounded-lg px-3 py-2 text-slate-200 hover:text-sky-400 transition ease-linear"
			>Open App</a
		>
		{:else}
		<a
			href="#"
			class="rounded-lg px-3 py-2 text-slate-200 hover:text-sky-400 transition ease-linear"
			on:click={login}
			>Login</a
		>
		{/if}
	</div>
</nav>
