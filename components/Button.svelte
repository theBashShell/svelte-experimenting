<script>
	export let count;  
</script>

{#if count === 10 }
<svelte:self count={--count} />
{/if} 

<h1>{count}</h1>