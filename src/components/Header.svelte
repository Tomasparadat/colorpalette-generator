<script>
  import { openModal } from "../store";
</script>

<header class="flex flex-col relative z-20">
  <div
    class="max-w-[1400px] mx-auto w-full flex items-center justify-between p-4 py-6"
  >
    <a href="/" class="font-semibold text-xl"
      ><h1>Palette <span class="text-indigo-500">Generator</span></h1></a
    >

    <button
      on:click={() => $openModal = true}
      class="md:hidden grid place-items-center"
      ><i class="fa-solid fa-bars"></i></button
    >

    <nav class=" hidden md:flex items-center gap-6 lg:gap-8">
      <a
        href="#Product"
        class="duration-200 hover:text-indigo-500 cursor-pointer">Product</a
      >
      <a
        href="#Reviews"
        class="duration-200 hover:text-indigo-500 cursor-pointer">Reviews</a
      >
      <a href="#FAQs" class="duration-200 hover:text-indigo-500 cursor-pointer"
        >FAQ</a
      >
    </nav>

    <button class="hidden md:flex specialBtn"><p>Start free today</p></button>
  </div>
</header>
