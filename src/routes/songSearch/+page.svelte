<script>
    let songSearch = {songname:"",singername:"",lyrics:"",videolink:"",songid:""}
    const handleSubmit=()=>{console.log("success!",songSearch);
    fetchLyricsOVH(songSearch)
    songSearch = {songname:"",singername:"",lyrics:"",videolink:"",songid:""} //immediately make input to nothing
    }

const fetchLyricsOVH = async (songSearch) => {
  // SetLoading(true);
  // const controller = new AbortController();
  // const TimeoutFunction = setTimeout(() => {
  //   console.warn("It's over 3 seconds, stop fetching");
  //   controller.abort();
  // }, 3000); //abort if it's over 3 seconds

  // if (!songSearch.singername?.trim() || !songSearch.songname?.trim()) {
  //   //return null if they submit empty string
  //   console.warn("Empty singer or song name. Fetch aborted.");
  //   SetLoading(false);
  //   return null;
  // }

  try {
    const songFetch = await fetch(
      `https://api.lyrics.ovh/v1/${songSearch.singername}/${songSearch.songname}`,
      // { signal: controller.signal },
    );
    // clearTimeout(TimeoutFunction); //clears if successful fetch
    console.log(songFetch);
    const songJson = await songFetch.json();
    console.log(songJson.lyrics);
    // SetLoading(false);
    return songJson.lyrics;
  } catch (error) {
    // clearTimeout(TimeoutFunction); //clears if failed fetch
    console.error("caught error:", error);
    // SetLoading(false);
    return null;
  }
};
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
    bind:value={songSearch.songname}
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
    bind:value={songSearch.singername}
  />
</div>

<button type="submit" class="flex">
  Get my lyrics
</button>
</form>



