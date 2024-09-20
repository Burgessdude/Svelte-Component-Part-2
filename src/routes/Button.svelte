<script>
	export let name = "Default";
	export let type = "regular"; // regular, flat, disabled
	export let size = "md"; // sm, md, lg
	const sizes = {
		"sm" : "px-1 py-3 pr-8 pl-8",
		"md" : "px-5 py-3 pr-8 pl-8",
		"lg" : "px-7 py-5 pr-8 pl-8",
	}
</script>

{#if type=="regular"}
 <button class={`bg-indigo-500 text-white font-medium h-12 w-80 rounded-full ${(size in sizes) ? sizes[size] : sizes["md"]}`}>
  {name}
 </button>
{/if}

{#if type=="flat"}
 <button class={`bg-indigo-700 text-white font-medium h-12 w-80 rounded-full text-center align-middle ${(size in sizes) ? sizes[size] : sizes["md"]}`}>
  {name}
 </button>
{/if}

{#if type=="disabled"}
 <button class={`bg-gray-400 text-gray-600 font-medium h-12 w-80 rounded-full ${(size in sizes) ? sizes[size] : sizes["md"]}`}>
  {name}
 </button> 
{/if}