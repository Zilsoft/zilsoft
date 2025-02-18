<script>
  let { y } = $props();
  let tabs = [
    { name: "Проекты", link: "#projects" },
    { name: "О Себе", link: "#about" },
  ];
</script>

<header
  class={"sticky z-10 top-0 duration-200 px-6 flex items-center justify-between border border-solid" +
    (y > 0
      ? "py-4 bg-slate-950 border-violet-950"
      : "py-6 bg-transparent border-transparent")}
>
  <h1 class="font-medium">
    <b class="font-bold lato">Дмитрий</b> Павлюков
  </h1>
  <div class="sm:flex ml-auto pr-4 items-center gap-4 hidden my-4">
    {#each tabs as tab, index}
      <a
        class="duration-200 hover:text-violet-400"
        aria-label="Ссылка {index}"
        href={tab.link}
      >
        <p>{tab.name}</p>
      </a>
    {/each}
  </div>
  <a
    href="#link"
    aria-label="Связаться"
    class="blueShadow group relative overflow-hidden px-5 py-2 rounded-full bg-white text-slate-950"
  >
    <div
      class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
    ></div>
    <h4 class="relative z-9">Связяться</h4>
  </a>
</header>
