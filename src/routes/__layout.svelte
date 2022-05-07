<script context="module">
  /** @type {import('@sveltejs/kit').Load} */
  export const load = async ({ url }) => ({ props: { url } });
</script>

<script>
  import Pagetransition from '../components/pagetransition.svelte';
  import Navbar from '../components/navbar.svelte';
  export let url;
</script>

<Navbar />
<Pagetransition {url}>
  <slot class="slot" />
</Pagetransition>

<style>
  .slot {
    display: grid;
    grid-template-columns: 1fr;
    grid-template-rows: 1fr;
  }
</style>
