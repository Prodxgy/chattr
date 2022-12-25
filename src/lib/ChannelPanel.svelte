<script lang="ts">
	import Channel from './Channel.svelte';
	const props = {
		img: 'https://ui-avatars.com/api/?name=John+Doe',
		name: 'John Doe',
		prev_msg:
			"Hey how are you. you do  you, thats why we got no issues but we're not stressesd out by our insecurities."
	};
</script>

<aside class="hidden lg:block fixed z-20 inset-0  w-[25rem] overflow-y-auto bg-slate-900">
	<section class="px-8 flex flex-col h-28 justify-between">
		<h1 class="py-8 mx-auto text-3xl font-extrabold text-slate-100 text-center">Conversations</h1>
		<hr />
	</section>
	<section class="h-[calc(100%-7rem)]">
		<Channel {...props} />
	</section>
</aside>
