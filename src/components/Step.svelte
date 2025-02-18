<script>
  let { step, children } = $props();
</script>

<a
  href={step.href}
  target="_blank"
  aria-label={step.name}
  class="p-4 sm:p-6 md:p-8 flex flex-col gap-4 rounded-lg border
  border-solid border-violet-700 text-center group cursor-pointer
   hover:border-violet-400 duration-200"
>
  <div
    class="bg-slate-950 grid place-items-center px-4 text-5xl md:text-6xl
    -mt-10 sm:-mt-12 md:-mt-14 lg:-mt-16 mx-auto duration-200"
  >
    <i class={step.icon}></i>
  </div>
  <h3 class="font-medium text-xl sm:text-2xl md:text-3xl">{step.name}</h3>
  {@render children?.()}
  <div class="flex-1 flex justify-between gap-4 items-center">
    <div
      class="ml-auto mt-auto cursor-pointer hover:text-violet-400 duration-200 overflow-hidden
    relative after:absolute after:top-0 after:right-full after:w-full after:h-full
    after:bg-violet-700 after:duration-200 after:z-[-1] hover:after:translate-x-full"
    >
      <p class="relative z-1">Ознакомиться &rarr;</p>
    </div>
  </div>
</a>
