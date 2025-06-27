<!-- Route/+page.svelte -->
<script>
let songSearch = $state("")
import SongSearch from "./songSearch/+page.svelte"
import Home from "./home/+page.svelte"
</script>

<style lang="postcss">
  @reference "tailwindcss";
  :global(html) {
    background-color: theme(--color-gray-500);
  }
</style>
