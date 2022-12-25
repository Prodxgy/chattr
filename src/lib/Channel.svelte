<script lang="ts">
	export let img: string;
	export let name: string;
	export let prev_msg: string;
</script>

<div class="mx-3 overflow-hidden after:block after:w-9/12 after:mx-auto after:my-0 after:border-b-1 after:border-b-slate-500">
	<a href="#" class="my-2 rounded-2xl flex flex-row w-full transition ease-in hover:bg-sky-600 duration-200">
		<img class="my-6 ml-6 rounded-full" src={img} alt="{name} Profile Picture" />
		<div class="m-3 p-2 my-auto text-slate-200 w-full truncate">
			<h1 class="font-extrabold text-2xl truncate ...">{name}</h1>
			<p class="h-full truncate ...">{prev_msg}</p>
		</div>
	</a>
</div>
