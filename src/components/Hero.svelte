<script>
  import SectionWrapper from "../components/SectionWrapper.svelte";
  import CtAs from "./CTAs.svelte";
  import Header from "./Header.svelte";
  import star from "$lib/images/star.svg";
  import wave from "$lib/images/wave.svg";
  import spiral from "$lib/images/spiral.svg";
  import arrow from "$lib/images/arrow.svg";
</script>

<SectionWrapper id="hero">
  <Header />
  <div
    class="flex flex-col gap-10 items-center justify-center flex-1 pb-10 md:pb-14"
  >
    <h2
      class="text-5xl sm:text-6xl md:text-7xl lg:text-8xl max-w-[1200px] mx-auto w-full text-center font-semibold tracking-tight"
    >
      <span class="text-indigo-500">Design</span>
      <span class="text-slate-500 line-through">Is Hard</span><br /> Just Got
      <span class="text-indigo-500">Easier</span>
    </h2>
    <p
      class="text-xl sm:text-2xl md:text-3xl text-slate-500 text-center max-w-[500px] mx-auto w-full"
    >
      We cut your design time in half by creating beautiful color palettes for
      your project.
    </p>
    <img
        src={star}
        alt="star"
        class="absolute invisible xl:visible z-[-10] top-40 left-[15rem] right-0"
      />

    <img src={wave} alt="wave" class="absolute invisible xl:visible z-[-10] left-[18rem] right-0 top-[30rem]" />

    <img src={spiral} alt="spiral" class="absolute invisible xl:visible z-[-10] right-[20rem] top-[9rem]">

    <img src={arrow} alt="arrow" class="absolute invisible xl:visible  z-[-10] right-[12rem] top-[25rem]">
    <CtAs />
  </div>
</SectionWrapper>
