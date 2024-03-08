<script>
  import ProductCard from "./ProductCard.svelte";
  import SectionWrapper from "./SectionWrapper.svelte";
  let productFeatures = [
    {
      featureList: [
        "Intuitive Color Selection",
        "RGB and Hex Code Input",
        "Random Color Generator",
        "Save and Share",
      ],
      description:
        "Effortlessly create unique color palettes, customize with RGB and hex code inputs and generate random combinations",
      imgUrl: "assets2/placeholder.jpg",
    },

    {
      featureList: [
        "Pre-designed Palettes",
        "Theme Matching",
        "Color Harmony Analysis",
        "Trendy Color Sets",
      ],
      description:
        "Discover curated palettes for diverse themes, explore color harmony analysis, and stay trendy with our latest color sets.",
      imgUrl: "assets2/placeholder.jpg",
    },

    {
      featureList: [
        "Live Preview",
        "Preview Templates",
        "Contrast Checker",
        "Color Blind Simulation",
      ],
      description:
        "Instantly visualize your color choices in various contexts with live previews, templates, contrast checking, and color-blind simulation tools.",
      imgUrl: "assets2/placeholder.jpg",
    },
  ];
</script>

<SectionWrapper id="Product">
  <div
    class="flex flex-col items-center justify-center gap-10 sm-gap-14 md:gap-24 flex-1 pb-10 md:pb-14"
  >
    <div class="flex flex-col gap-2">
      <p class="opacity-60 text-base sm:text-lg md_text-xl text-center">
        Start your enhanced <span class="text-indigo-500">design journey</span> today
      </p>
      <h3
        class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full text-center font-semibold"
      >
        Features For Everyone
      </h3>
    </div>

    {#each productFeatures as productFeature, index}
      <ProductCard {productFeature} {index}>
        {#if index === 0}
          Custom <span class="text-indigo-500">Color Palette</span> Creation
        {:else if index === 1}
          <span class="text-indigo-500">Color</span> Scheme Suggestions
        {:else}
          <span class="text-indigo-500">Visualization</span> Tools
        {/if}
      </ProductCard>
    {/each}
  </div>
</SectionWrapper>
