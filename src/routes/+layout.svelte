<script>
  import "../app.css";
  import Footer from "../components/Footer.svelte";

  import { openModal } from "../store";

  let y;
  $: outerHeight = 0;

  function reroute(href) {}
</script>

{#if $openModal}
  <div
    class="fixed top-0 left-0 w-screen h-screen border-b bg-white z-50 flex flex-col gap-8 p-5 px-8 md:hidden"
  >
    <div class="flex items-center justify-between gap-4 border-b pb-2">
      <h1>Palette <span class="text-indigo-500">Generator</span></h1>
      <button
        on:click={() => ($openModal = false)}
        class="border-none outline-none"
      >
        <i class="fa-solid fa-xmark fa-2xl"></i>
      </button>
    </div>
    <div class="flex flex-col gap-4">
      <button
        on:click={() => reroute("#Product")}
        class="border-none outline-none p-2 group text-left cursor-pointer"
        ><p class="duration-200 group-hover:pl-2">Product</p></button
      >

      <button
        on:click={() => reroute("#Reviews")}
        class="border-none outline-none p-2 group text-left cursor-pointer"
        ><p class="duration-200 group-hover:pl-2">Reviews</p></button
      >

      <button
        on:click={() => reroute("#FAQs")}
        class="border-none outline-none p-2 group text-left cursor-pointer"
        ><p class="duration-200 group-hover:pl-2">FAQ</p></button
      >
    </div>
    <button class="specialBtn max-w-[180px] mx-auto">Try free today</button>
  </div>
{/if}

<slot />
<Footer />
<svelte:window bind:scrollY={y} bind:outerHeight />
