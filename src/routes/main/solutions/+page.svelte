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

</script>

<main class="grid grid-flow-col auto-cols-max overflow-x-auto overscroll-contain snap-y">
  <div class="w-screen h-screen flex flex-col justify-center items-center bg-slate-950 snap-center">
    <h1 class="text-4xl font-bold text-transparent bg-clip-text bg-gradient-to-r from-blue-500 to-blue-800">
      <TypeWriter texts={['What are the solutions to biodiversity loss?']} />
    </h1>
    <span class="text-gray-400 m-4">
      scroll to see more
    </span>
  </div>

  <div class="w-screen h-full flex justify-center items-center overflow-hidden bg-slate-950 snap-center">
    <div class="text-white text-3xl w-[60vw]">
      <p>
                In <strong class="strongtext">our</strong> lifetime, we can take a few actions to minimise the effects of this phenomenon, and if we all work <strong class="strongtext">together,</strong> we might be able to make a difference.
      </p>
    </div>
  </div>
  <div class="w-screen h-full flex justify-center items-center overflow-hidden bg-slate-950 snap-center ">
     <div class="w-[50vw] h-auto bg-gray-900 border-gray-600/10 border-2 rounded-2xl p-6 ">
        <img src="https://media.istockphoto.com/id/157366413/photo/power-plant-in-the-sunrise.jpg?s=612x612&w=0&k=20&c=63l2ulDEx3Syx3_cw5nBbNoF0RMXT7visxSWnMWyngA="/>
        <span class="text-white font-bold text-2xl">
            Solution 1: Reduce our carbon footprint
        </span>

        <p class="text-white">
            Carbon emissions plays a massive role in the development of biodiversity loss, and the less carbon we emit the more we can slow down the effects of it. An example of this is using renewable energy, either by installing solar panels or using a green tarriff from your energy providerds.
        </p>
    </div>
    <div class="w-[50vw] h-auto bg-gray-900 border-gray-600/10 border-2 rounded-2xl p-6 m-2">
        <img src="https://media.istockphoto.com/id/922735808/photo/the-day-the-world-changed-concept.jpg?s=612x612&w=0&k=20&c=LXd4H2YJ5skivtN81sRT0hSzQJxNM9W27ulDUOaLX6o=" alt="">
        <span class="text-white font-bold text-2xl">
            Solution 2: Preserve the ecosystems
        </span>

        <p class="text-white">
            Different servieces exist where you can adopt animals, such as the WWF. Adopting an animal could help to save that species and rehabilitate it's chance of survival, reducing the effects of biodiversity loss and potentially bringing an ecosystem back ontoo it's feet. An example of this is the Pandas you can adopt on the WWF website.
        </p>
    </div>
    <div class="w-[50vw] h-auto bg-gray-900 border-gray-600/10 border-2 rounded-2xl p-6 ">
        <img src="https://media.istockphoto.com/id/1334543278/photo/swarm-of-spotted-lanternflies.jpg?s=612x612&w=0&k=20&c=H_UQc-wLHptsBrYBwDI6Iu8sN0G-aDDVo3fHXxBBWgg=" alt="">
        <span class="text-white font-bold text-2xl">
            Solution 3: Reduce invasive species
        </span>

        <p class="text-white">
            As you have seen, invasive species can tear apart ecosystems and destroy species as they have no natural predators. You can help combat this by checking your shoes for seeds or other stuff that could spread.
        </p>
    </div>
</div>

<div class="bg-slate-950 h-screen w-full flex justify-center items-center overflow-hidden snap-center">
<a href="/main">
        <button type="button" class="text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-full text-sm p-2.5 text-center inline-flex items-center me-2 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">
        <span class="text-lg p-3">
            Back to main
        </span>
        <svg class="w-4 h-4" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 14 10">
            <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M1 5h12m0 0L9 1m4 4L9 9"/>
        </svg>
    </button>
</a>
</div>
</main>
<style>
  .strongtext {
    color: #4e54ff;
  }
</style>