<script lang="ts">
  import projects from "./projects.json";
</script>

<main
  class="box-border flex relative flex-col shrink-0 ml-[calc(50%_-_50vw)] h-auto landscape:h-screen overflow-hidden"
  style="background-color:#f5e8dd;"
>
  <header
    class="flex flex-col justify-center items-center m-5"
  >
    <h1 class="text-6xl">Projects</h1>
    <br />
    <div class="flex gap-2">
        <button
        class="bg-transparent font-semibold py-2 px-4 border border-black hover:border-white rounded"
        >
        <a href="/#home">
            <svg xmlns="http://www.w3.org/2000/svg" x="0px" y="0px" width="25" height="25" viewBox="0 0 30 30">
                <path d="M 15 2 A 1 1 0 0 0 14.300781 2.2851562 L 3.3925781 11.207031 A 1 1 0 0 0 3.3554688 11.236328 L 3.3183594 11.267578 L 3.3183594 11.269531 A 1 1 0 0 0 3 12 A 1 1 0 0 0 4 13 L 5 13 L 5 24 C 5 25.105 5.895 26 7 26 L 23 26 C 24.105 26 25 25.105 25 24 L 25 13 L 26 13 A 1 1 0 0 0 27 12 A 1 1 0 0 0 26.681641 11.267578 L 26.666016 11.255859 A 1 1 0 0 0 26.597656 11.199219 L 25 9.8925781 L 25 6 C 25 5.448 24.552 5 24 5 L 23 5 C 22.448 5 22 5.448 22 6 L 22 7.4394531 L 15.677734 2.2675781 A 1 1 0 0 0 15 2 z M 18 15 L 22 15 L 22 23 L 18 23 L 18 15 z"></path>
            </svg>
        </a>
        </button>
        <button
        class="bg-transparent font-semibold py-2 px-4 border border-black hover:border-white rounded"
        >
            <a href="https://github.com/rmore4623" target="_blank">
                <svg xmlns="http://www.w3.org/2000/svg" x="0px" y="0px" width="25" height="25" viewBox="0 0 64 64">
                    <path d="M32 6C17.641 6 6 17.641 6 32c0 12.277 8.512 22.56 19.955 25.286-.592-.141-1.179-.299-1.755-.479V50.85c0 0-.975.325-2.275.325-3.637 0-5.148-3.245-5.525-4.875-.229-.993-.827-1.934-1.469-2.509-.767-.684-1.126-.686-1.131-.92-.01-.491.658-.471.975-.471 1.625 0 2.857 1.729 3.429 2.623 1.417 2.207 2.938 2.577 3.721 2.577.975 0 1.817-.146 2.397-.426.268-1.888 1.108-3.57 2.478-4.774-6.097-1.219-10.4-4.716-10.4-10.4 0-2.928 1.175-5.619 3.133-7.792C19.333 23.641 19 22.494 19 20.625c0-1.235.086-2.751.65-4.225 0 0 3.708.026 7.205 3.338C28.469 19.268 30.196 19 32 19s3.531.268 5.145.738c3.497-3.312 7.205-3.338 7.205-3.338.567 1.474.65 2.99.65 4.225 0 2.015-.268 3.19-.432 3.697C46.466 26.475 47.6 29.124 47.6 32c0 5.684-4.303 9.181-10.4 10.4 1.628 1.43 2.6 3.513 2.6 5.85v8.557c-.576.181-1.162.338-1.755.479C49.488 54.56 58 44.277 58 32 58 17.641 46.359 6 32 6zM33.813 57.93C33.214 57.972 32.61 58 32 58 32.61 58 33.213 57.971 33.813 57.93zM37.786 57.346c-1.164.265-2.357.451-3.575.554C35.429 57.797 36.622 57.61 37.786 57.346zM32 58c-.61 0-1.214-.028-1.813-.07C30.787 57.971 31.39 58 32 58zM29.788 57.9c-1.217-.103-2.411-.289-3.574-.554C27.378 57.61 28.571 57.797 29.788 57.9z"></path>
                </svg>
            </a>
        </button>
    </div>
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
            class="absolute inset-0 flex flex-col justify-center items-center rounded-xl [backface-visibility:hidden] [transform:rotateY(180deg)] shadow-xl shadow-black/40"
            style="background-color:{project.primary_color}"
          >
            <div
              class="absolute justify-center items-center px-3 py-3 inset-0 flex flex-col text-[{project.secondary_color}] [word-wrap:break-word]"
            >
              <h1 class="text-xl">{project.title}</h1>
              <br />
              <p>{project.description}</p>
            </div>
          </div>
        </article>
      {/each}
    </div>
  </section>
</main>
