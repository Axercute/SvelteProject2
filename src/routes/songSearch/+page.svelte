<script lang="ts">
    const handleSubmit=()=>{console.log("success")}
    let songNameSearch=""
    let singerNameSearch=""
    const wow =(event)=>{console.log(event.target.value)}
</script>

       <form on:submit|preventDefault={handleSubmit}
        class="flex-center mx-auto w-1/3 flex-col flex-wrap rounded-3xl border-2
         bg-gradient-to-br from-fuchsia-950 to-amber-700 mt-3">
        <div class="flex flex-row my-2">

        <label for="songname" class="text-outline w-28">
        Song Name:
        </label>
          <input
            id="songname"
            name="songname"
            type="text"
            placeholder="Billie Jean"
            bind:value={songNameSearch}
            on:input={wow}
          />
        </div>

        <div class="flex flex-row">
          <label for="singername" class="text-outline w-28">
            Singer Name:
          </label>
          <input
            id="singername"
            name="singername"
            type="text"
            placeholder="Michael Jackson"
            bind:value={singerNameSearch}
          />
        </div>

        <button type="submit" class="flex">
          Get my lyrics
        </button>
      </form>



