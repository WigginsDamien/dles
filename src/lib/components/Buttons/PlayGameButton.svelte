<script>
  import { filteredDles } from "$lib/stores"
  import IconPlay from "../Icons/IconPlay.svelte"
  import MenuRandom from "../MenuRandom.svelte"
  import Random from "../MenuRandom.svelte"
  import DropdownMenuButton from "./DropdownMenuButton.svelte"
  let url = ""
  let dle = {
    url,
  }

  function randomDle() {
    let randomIndex = Math.floor(Math.random() * $filteredDles.length)
    return $filteredDles[randomIndex]
  }

  async function playRandomDle() {
    dle = randomDle()
    this.parentElement.href = dle.url
    setTimeout(() => {
      this.parentElement.href = "?random"
    }, 300)
  }
</script>

<DropdownMenuButton name="random-menu">
  <div slot="menu">
    <MenuRandom />
  </div>
</DropdownMenuButton>

<!-- <div class="text-xs mx-auto">(Opens in new tab)</div> -->
