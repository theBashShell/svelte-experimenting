<script>
	let count = 0;
	import { createEventDispatcher } from "svelte";

	let dispatch = createEventDispatcher();

	function handleClick() {
	  count += 1;
	  dispatch("message", {
	    text: "hello"
	  });
	}
</script>

<style>
	button {
	  background: #644236;
	  color: white;
	  border: none;
	  padding: 8px 12px;
	  border-radius: 2px;
	}
</style>

<button on:click={handleClick}>
  Clicked {count} {count === 1 ? 'time' : 'times'}
</button>