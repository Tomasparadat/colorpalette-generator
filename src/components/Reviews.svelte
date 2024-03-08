<script>
  import ReviewCard from "./ReviewCard.svelte";
  import SectionWrapper from "./SectionWrapper.svelte";

  let lim = true;

  let reviewsList = [
    {
      name: "Emily",
      review:
        "Absolutely fantastic! Color Palette Generator has revolutionized my design process. The color palettes it generates are always spot-on and perfectly complement each other.",
      features: [
        "Intuitive interface",
        "Customizable palettes",
        "Easy export options",
      ],
    },
    {
      name: "Alex",
      review:
        "PaletteMaster is a game-changer! As a graphic designer, I rely on it daily for inspiration. Its ability to suggest harmonious color schemes is unparalleled.",
      features: [
        "Vast color library",
        "Real-time preview",
        "Cross-platform compatibility",
      ],
    },
    {
      name: "Sophia",
      review:
        "I've tried several color palette generators, but ColorBlend stands out. Its AI algorithms seem to understand my preferences better than I do!",
      features: [
        "Smart suggestion algorithm",
        "Dark mode support",
        "Detailed color information",
      ],
    },
    {
      name: "Liam",
      review:
        "ChromaPulse is a dream come true for anyone struggling with color combinations. It takes the guesswork out of the equation and delivers stunning palettes effortlessly.",
      features: [
        "Interactive color wheel",
        "Instant color grading",
        "Palette sharing options",
      ],
    },
    {
      name: "Ava",
      review:
        "PaletteWizard is my secret weapon for creating visually appealing designs. Its simplicity combined with powerful features makes it indispensable in my toolkit.",
      features: [
        "Drag-and-drop functionality",
        "History of generated palettes",
        "Export to popular formats",
      ],
    },
    {
      name: "Noah",
      review:
        "ColorHarmonizer is a gem for artists and designers alike. I love how it suggests both traditional and unconventional color schemes, sparking creativity at every turn.",
      features: [
        "Multiple color harmony types",
        "Palette customization options",
        "Color contrast analysis",
      ],
    },
    {
      name: "Mia",
      review:
        "HueMagic truly lives up to its name! It's like having a color expert in your pocket. Whether I need vibrant palettes or subtle shades, it delivers with finesse.",
      features: [
        "Color gradient generator",
        "Palette history tracking",
        "Cloud sync for seamless access",
      ],
    },
    {
      name: "William",
      review:
        "ColorCraft has simplified my workflow immensely. The ability to fine-tune palettes and preview them in real-time has saved me countless hours of trial and error.",
      features: [
        "Live preview mode",
        "Advanced color blending",
        "Palette export to Adobe software",
      ],
    },
    {
      name: "Ella",
      review:
        "PalettePro is a must-have for anyone serious about design. Its robust feature set empowers users to explore endless color combinations with ease.",
      features: [
        "Color theory tutorials",
        "Palette customization tools",
        "Integration with design software",
      ],
    },
    {
      name: "James",
      review:
        "ChromaGenius is my go-to tool for crafting cohesive color schemes. The curated palettes it generates always exceed my expectations, making my designs shine.",
      features: [
        "Palette randomization",
        "Colorblind-friendly mode",
        "Export to CSS and SVG",
      ],
    },
  ];
</script>

<SectionWrapper id="Reviews">
  <div
    class="flex flex-col gap-10 sm:gap-24 py-20 flex-1 items-center justify-center"
  >
    <div class="flex flex-col gap-2">
      <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">
        Don't take our word for it
      </p>
      <h3
        class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"
      >
        See What <span class="text-indigo-500">Others</span> Have To Say
      </h3>
    </div>

    <div class="flex flex-col md:flex-row gap-8 w-fit mx-auto">
      <div class="flex flex-col gap-8">
        {#each lim ? reviewsList.slice(0, 4) : reviewsList as reviewItem, index}
          <ReviewCard {reviewItem} left={true} {index} />
        {/each}
      </div>

      <div class="w-[1px] bg-slate-950 hidden md:flex"></div>

      <div class="flex flex-col gap-8">
        {#each lim ? reviewsList.slice(0, 4) : reviewsList as reviewItem, index}
          <ReviewCard {reviewItem} {index} />
        {/each}
      </div>
    </div>
    <button on:click={() => (lim = !lim)} class="specialBtnViolet">
      <p>{lim ? "Show More" : "Show Less"}</p></button
    >
  </div>
</SectionWrapper>
