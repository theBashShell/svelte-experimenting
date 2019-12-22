<script>
  import { createEventDispatcher } from "svelte";
  import Button from "./Button.svelte";
  let list = [0, 1, 23, 3];
import {theme} from '../store.js'

let t = ''
  let dispatch = createEventDispatcher();

const unsubscribe = theme.subscribe(a => t = a)
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
<h1>{console.log(theme)}</h1>
<h1>{t}</h1>