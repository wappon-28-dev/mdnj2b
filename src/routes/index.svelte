<script lang="ts">
  import Button, { Icon, Label } from "@smui/button";
  import { firestoreStatus, isLoading, sampleData } from "$lib/store";
  import { onMount } from "svelte";
  import Home from "./_home.svelte";
  import Trailer from "./_trailer.svelte";
  import Place from "./_place.svelte";
  import Rules from "./_rules.svelte";
  import Etc from "./_etc.svelte";

  onMount(() => {
    isLoading.set(false);
  });

  let status = "";
  firestoreStatus.subscribe((value) => (status = value));
</script>

<div id="home">
  <Home />
</div>
<div id="trailer">
  <Trailer />
</div>
<div id="place">
  <Place />
</div>
<div id="rules">
  <Rules />
</div>
<div id="etc">
  <Etc />
</div>

<style>
</style>
