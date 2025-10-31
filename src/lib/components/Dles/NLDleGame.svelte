<script>
  import { settings } from "$lib/stores"
  import BackToTopButton from "../Buttons/BackToTopButton.svelte"
  import DlesByCategory from "./DlesByCategory.svelte"
  import DlesByCategoryNoScript from "./DlesByCategoryNoScript.svelte"
  import DlesDetailed from "./DlesDetailed.svelte"
  import dles_json from "$lib/data/nldle.json"
</script>

<div>
  <pre>{JSON.stringify(dles_json, null, 2)}</pre>    THIS IS THE GAME
</div>

<BackToTopButton />
