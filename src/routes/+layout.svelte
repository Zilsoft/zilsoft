<script>
  let { children } = $props();
  import "../app.css";
  import Header from "../components/Header.svelte";
  import Footer from "../components/Footer.svelte";
  let y = $state();
  let innerHeight = $state(0);
  let innerWidth = $state(0);
  function goTop() {
    document.body.scrollIntoView();
  }
</script>

<div
  class="relative flex flex-col max-w-[1400px] min-h-screen mx-auto w-full text-sm sm:text-base"
>
  <div
    class={"fixed bottom-0 w-full duration-200 flex p-10 z-10" +
      (y > 0
        ? "opacity-full pointer-events-auto"
        : "opacity-0 pointer-events-none")}
  >
    <button
      onclick={goTop}
      aria-label="Вернуться наверх"
      class="ml-auto rounded-full aspect-square bg-slate-900 text-violet-400 px-3 sm:px-4 hover:bg-slate-800 cursor-pointer"
    >
      <i class="fa-solid fa-arrow-up"></i>
    </button>
  </div>
  <Header {y} />
  {@render children?.()}
  <Footer />
</div>
<svelte:window bind:scrollY={y} bind:innerHeight bind:innerWidth />
