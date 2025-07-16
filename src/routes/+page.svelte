<script>
</script>
<main>
  <section class="section1">
    <h1 class="headerText">AUSTRALIAN BIODIVERSITY LOSS</h1>
  </section>
  <div class="image"></div>
  <section class="section2">
    <button id="btn" class="relative py-1 px-2 bg-zinc-900 rounded-full group after:content-[''] after:group after:absolute after:h-[107%] after:w-[102%] after:rounded-full flex justify-center items-center after:z-[-1]">
      <a href="/main/">
        <h1 class="gradient-text">click to see more <span class="inline-block transition-transform group-hover:translate-x-3">-> &nbsp;</span> </h1>
      </a>

    </button>
  </section>
</main>

<style>
  main {
    height: 100vh;
    overflow-y: auto;
    overflow-x: hidden;
    perspective: 1px;
    transform-style: preserve-3d;
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

  .section1 .headerText {
    position: relative;
    z-index: 5;
    font-family: "Oswald", sans-serif;
    font-size: 6.5vw;
    color: white;
    text-align: center;
    text-shadow:
      2px 2px 5px rgba(0,0,0,0.3),
      5px 5px 70px rgba(255,255,255,0.5);
    transform: translateY(20vh);
  }
  .headerText {
    font-family: "Oswald", sans-serif;
  }
  .section1 {
    display: flex;
    justify-content: center;
    align-items: center;
    overflow: hidden;
    width: 100vw;
  }

  .section2 {
    background: #1c1c1c;
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
  #btn::after {
    background-image: linear-gradient(to bottom right, #008cff, #e100ff);
 }
  #btn:hover {
    z-index: 0;
    box-shadow: 40px 0 100px #008cff85, -40px 0 -100px #e100ffbb
  }
 .gradient-text {
  font-size: 3rem;
  font-weight: bold;
  background: linear-gradient(to bottom right, #008cff, #e100ff);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  color: transparent;
  padding: 1.5rem;
  transition: color 0.3s ease;
}

.gradient-text:hover {
  background: none;
  -webkit-background-clip: unset;
  -webkit-text-fill-color: unset;
  background-clip: unset;
  color: white;
}

</style>
