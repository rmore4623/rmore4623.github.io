<script lang="ts">
  import projects from "./projects.json";
</script>

  <main
    class="box-border flex relative flex-col shrink-0 ml-[calc(50%_-_50vw)] h-auto landscape:h-screen overflow-hidden" style="background-color:#f5e8dd;"
  >
    <header class="box-border flex flex-col relative shrink-0 justify-center self-center items-center m-5 h-auto">
        <h1>Projects</h1>
        <br />
        <button class="bg-transparent hover:bg-blue-500 text-blue-700 font-semibold hover:text-white py-2 px-4 border border-blue-500 hover:border-transparent rounded">
            <a href="/#home">Home</a>
        </button>
    </header>


    <section class="box-border flex flex-col shrink-0 mx-5 my-5 h-auto">
        <!-- needs refactoring here -->
      <div
        class="relative flex gap-5 flex-col justify-center items-center md:items-start md:flex-row"
      >
        {#each projects as project}
          <article
            class="relative w-full md:w-6/12 hover:[transform:rotateY(180deg)] [transform-style:preserve-3d] transition-all duration-500 ease-in"
          >
            <div
              id="frontside"
              class="flex flex-col [backface-visibility:hidden] rounded-xl"
              style="background-color:#e2e3e5"
            >
              <img
                loading="lazy"
                src={project.src}
                alt={project.alt}
                style="fit:cover"
                class="box-borderobject-contain overflow-hidden rounded-xl px-5 py-5 shrink-0 mt-5 w-full aspect-[1.42] min-h-[20px] min-w-[20px] shadow-xl shadow-black/40"
              />
            </div>
            <div
              id="backside"           
              class="absolute inset-0 flex flex-col justify-center items-center rounded-xl px-3 [backface-visibility:hidden] [transform:rotateY(180deg)] shadow-xl shadow-black/40"
              style="background-color:{project.primary_color}"
            >
              <div class="absolute inset-0 flex flex-col">
                <h1>{project.title}</h1>
                <br />
                <p>{project.description}</p>
              </div>
            </div>
          </article>
        {/each}
      </div>
    </section>
  </main>
