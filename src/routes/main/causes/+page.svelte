<script lang="ts">
  import { onMount } from 'svelte'
  import {TypeWriter} from 'svelte-typewrite';

  onMount(() => {
    if (typeof window !== 'undefined') {
      const mains = document.querySelectorAll('main')
      mains.forEach(main => {
        main.addEventListener('wheel', e => {
          e.preventDefault()
          main.scrollLeft += e.deltaY
        }, { passive: false })
      })
    }
  })
  let _class: string = "";
  export { _class as class };

  import { cn } from "$lib/utils";
  import { Motion } from "svelte-motion";

  let position = { x: 0, y: 0 };
  let ref: HTMLButtonElement | null = null;

  let handleMouseMove = (e: MouseEvent) => {
    let { clientX, clientY } = e;
    let { height, width, left, top } = ref.getBoundingClientRect();

    let middleX = clientX - (left + width / 2);
    let middleY = clientY - (top + height / 2);

    position.x = middleX;
    position.y = middleY;
  };

  let handleMouseLeave = () => {
    position.x = 0;
    position.y = 0;
  };
</script>

<main class="grid grid-flow-col auto-cols-max overflow-x-auto overscroll-contain snap-y">
  <div class="w-screen h-screen flex flex-col justify-center items-center bg-slate-950 snap-center">
    <h1 class="text-4xl font-bold text-transparent bg-clip-text bg-gradient-to-r from-red-500 via-red-600 to-red-800">
      <TypeWriter texts={['What is biodiversity loss in Australia?']} />
    </h1>
    <span class="text-gray-400 m-4">
      scroll to see more
    </span>
  </div>

  <div class="w-screen h-full flex justify-center items-center overflow-hidden bg-slate-950 snap-center">
    <div class="text-white text-3xl w-[60vw]">
      <p>
        <span class="strongtext">Biodiversity loss</span> is a phenomenon whereby the <span class="strongtext">population of animals</span> in a certain area <span class="strongtext">decreases</span> due to many factors. <span class="strongtext">In Australia,</span> examples of animals that are affected include: <span class="strongtext">Koalas,</span> <span class="strongtext">Tasmanian devils,</span> and Northern hairy-nosed <span class="strongtext">wombats.</span> 
      </p>
    </div>
  </div>
  <div class="w-screen h-full flex justify-center items-center overflow-hidden bg-slate-950 snap-center ">
    <h1 class="text-4xl font-bold text-transparent bg-clip-text bg-gradient-to-r from-red-500 via-red-600 to-red-800">
      <Motion
  let:motion
  animate={{ x: position.x, y: position.y }}
  transition={{
    type: "spring",
    damping: 15,
    stiffness: 150,
    mass: 0.1,
  }}
>
  <a href="/main/causes/why" class="hover:cursor-pointer">
    <button
    class={cn(
      "relative rounded-xl bg-white px-4 py-2 text-2xl font-semibold text-black",
      _class
    )}
    bind:this={ref}
    on:mousemove={handleMouseMove}
    on:mouseleave={handleMouseLeave}
    use:motion
  >
    <slot>But Why?</slot> 
  </button>
  </a>
</Motion>
    </h1>
  </div>
</main>
<style>
  .strongtext {
    color: #ff4e6c;
  }
</style>