<svelte:head>
    <title>Kawaii Hamsuke</title> 
</svelte:head>

<script>
  import { hamList } from "../hamList";
  // import { Card } from "../components/Card.svelte";
</script>

<div class="w-screen min-h-screen bg-white align-middle">
  <div class="w-screen bg-gray- p-6 pl-8 md:pl-16 border-b-4 border-primary mb-16">
    <img src="icon_cuteham.png" class="w-48" alt="logo" />
  </div>
  <div class="container mx-auto">
    <div class="flex flex-wrap justify-center">
      {#each hamList as ham}
        <div class="px-4 mb-8">
          <div class=" px-4 mb-8">
            <div class="relative w-full h-fit">
              <img style="max-width:300px;" class="aspect-video object-fill" src={ham.img} alt={ham.hamName}>
            </div>
            <div class="mt-2">
              <h2 class="text-xl font-semibold text-black">{ham.hamName}</h2>
            </div>
          </div>
        </div>
      {/each}
    </div>
  </div>
</div>
