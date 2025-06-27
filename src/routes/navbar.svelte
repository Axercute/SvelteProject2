<script>
    import {goto} from "$app/navigation"

    const navBarInfo = [
    {display:"Home", path:"home"},
    {display:"Song Search", path:"songSearch"},
    {display:"Song Login", path:"songLogin"},
    {display:"Contact Us", path:"contactUs"},
    ]
</script>
<div class="- text-center">
    <nav>
        {#each navBarInfo as {display,path}}
        <a href="/{path}" onclick={()=>{}}>{display}</a>
        {/each}
    </nav>
</div>

<style lang="postcss">
  @reference "tailwindcss";
</style>