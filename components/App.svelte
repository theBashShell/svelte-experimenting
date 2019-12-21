<script>
  import Button from "./Button.svelte";
  let list = [0, 1, 23, 3];
</script>

<style>
  div {
    height: 20px;
    background: wheat;
    margin: 20px;
  }
</style>

<main>
	{#each list as val, i }
<div>{i} --- {val}</div>
{/each}
</main>