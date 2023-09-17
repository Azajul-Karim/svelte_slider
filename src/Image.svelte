<script>
  import { createEventDispatcher } from "svelte";
  const fire = createEventDispatcher();

  export let slider = {};
  export let index;
</script>

<div class="container">
  <div
    on:click={(event) => fire("active_slider", { index })}
    class="panel {slider.active ? 'active' : ''}"
    style="background-image: url('{slider.url}') "
  >
    <h3>{slider.name}</h3>
  </div>
</div>
