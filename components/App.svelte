<script>
  import { createEventDispatcher } from "svelte";
  import Button from "./Button.svelte";
  let list = [0, 1, 23, 3];

  let dispatch = createEventDispatcher();
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

<Button on:message={(event) => console.log(event.detail.text)} />