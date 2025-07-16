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
    <h1 class="text-4xl font-bold text-transparent bg-clip-text bg-gradient-to-r from-green-500 to-green-800">
      <TypeWriter texts={['What are the effects of biodiversity loss on the environment?']} />
    </h1>
    <span class="text-gray-400 m-4">
      scroll to see more
    </span>
  </div>

  <div class="w-screen h-full flex justify-center items-center overflow-hidden bg-slate-950 snap-center">
    <div class="text-white text-3xl w-[60vw]">
      <p>
        Biodiversity loss can have <strong class="strongtext">many negative</strong> effects on the environment including <strong class="strongtext">ecosystem destruction</strong> and <strong class="strongtext">loss of vital services</strong> including water purification and <strong class="strongtext">climate regulation.</strong> 
      </p>
    </div>
  </div>
  <div class="w-screen h-full flex justify-center items-center overflow-hidden bg-slate-950 snap-center ">
     <div class="w-[50vw] h-auto bg-gray-900 border-gray-600/10 border-2 rounded-2xl p-6 ">
        <img src="https://natureaccordingtosam.wordpress.com/wp-content/uploads/2020/10/6115517604_3498272b91_k.jpg?w=1024" alt="">
        <span class="text-white font-bold text-2xl">
            Effect 1: ecosystem collapse
        </span>

        <p class="text-white">
            As biodiversity grows, the animals in an ecosystem have less food to feed off of and this eventually leads to major ecysystem imbalance, which can lead to sudden collapse, which has a whole world of other consequences. An example is the mangrove forests that used to exist on the coast, which have been almost completely wiped out.
        </p>
    </div>
    <div class="w-[50vw] h-auto bg-gray-900 border-gray-600/10 border-2 rounded-2xl p-6 m-2">
        <img src="https://media.istockphoto.com/id/1323415950/photo/corn-plants-wilting-and-dead-in-cornfield-herbicide-damage-drought-and-hot-weather-concept.jpg?s=612x612&w=0&k=20&c=Fui3pq__Hc1eIMzGo--H-usC_XPsrmdF1ouCbrP7poI=" alt="">
        <span class="text-white font-bold text-2xl">
            Effect 2: Food shortage
        </span>

        <p class="text-white">
            As numbers of certain species go down, it becomes less easy to find. As a result, we have less of them to eat, or their predators have less of them to eat, so they decrease in number. This can result in food shortage for humans. 
        </p>
    </div>
    <div class="w-[50vw] h-auto bg-gray-900 border-gray-600/10 border-2 rounded-2xl p-6 ">
        <img src="https://cdn.pixabay.com/photo/2016/12/17/14/33/wave-1913559_1280.jpg" alt="">
        <span class="text-white font-bold text-2xl">
            Effect 3: Extreme weather events
        </span>

        <p class="text-white">
            As some species start to diminish, their role in the ecosystem may not be filled in, and may result in major consequences for other species, or possibly entirely other ecosystems. For example: the mangrove forests in Australia have almost disappeared, putting them at risk of attack through water, such as flodding or a tsunami.
        </p>
    </div>
</div>
<div class="w-screen h-full flex justify-center items-center overflow-hidden bg-slate-950 snap-center">
    <img src="https://ichef.bbci.co.uk/ace/standard/976/cpsprodpb/17F1A/production/_105747089_wild_food-nc.png.webp" alt="" class="h-[500px] w-auto">
    <br>
    <span class="text-2xl text-white p-2">This graph shows the amount of food shortage around the world and where there is more biodiversity loss there is more food shortage.</span>
</div>
</main>
<style>
  .strongtext {
    color: #6cff4e;
  }
</style>