<main>
  <section class="section1">
    <h1 class="headerText">AUSTRALIAN BIODIVERSITY LOSS</h1>
    </section>
  <div class="image"></div>
  <section class="section2">
    <div class="group border border-solid rounded-full border-white/10 hover:bg-gray-200/5 ease-in-out duration-300">
      <a href="/main/" class="webkit bg-blur-3xl">
        <h1 class="headerText p-6">click to see more <span class="inline-block transition-transform group-hover:translate-x-3">-> &nbsp;</span> </h1>
      </a>
    </div>
  </section>
</main>

<style>
  main {
    height: 100vh;
    overflow-y: auto;
    overflow-x: hidden;
    perspective: 1px;
    perspective-origin: center center;
  }

  section {
    position: relative;
    min-height: 100vh;
    transform-style: preserve-3d;
  }

  .section1::before {
    content: "";
    position: absolute;
    top: 0; left: 0;
    width: 100%;
    height: 100%;
    background: url('/uluru.jpg') center center / cover no-repeat;
    transform: translateZ(-1px) scale(2);
    z-index: -1;
  }

  .image {
    position: absolute;
    bottom: 0; left: 0;
    width: 100%;
    height: 30vh;
    background: url('/uluru-ground.jpg') center bottom cover no-repeat;
    z-index: 10;
    pointer-events: none;
  }

  .section1 .headerText {
    position: relative;
    z-index: 5;
    font-family: 'Oswald', sans-serif;
    font-size: 6.5vw;
    color: white;
    text-align: center;
    text-shadow:
      2px 2px 5px rgba(0,0,0,0.3),
      5px 5px 70px rgba(255,255,255,0.5);
    transform: translateY(20vh);
  }

  .section1 {
    display: flex;
    justify-content: center;
    align-items: center;
    overflow: hidden;
    width: 100vw;
  }

  .section2 {
    background: #210800;
    color: white;
    text-align: center;
    text-shadow:
      2px 2px 5px rgba(0,0,0,0.3),
      5px 5px 70px rgba(255,255,255,0.5);
    display: flex;
    justify-content: center;
    align-items: center;
    font-family: "Oswald", sans-serif;
    font-size: 6vw;
  }
</style>
