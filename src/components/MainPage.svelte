<script>
    function downloadResume() {
      const a = document.createElement('a');

      a.href = '/files/Resume.pdf';
      a.download = 'romans_resume.pdf';
      a.click();
    }

    function scrollTo(event, sectionId) {
      event.preventDefault();
      const section = document.getElementById(sectionId);
      section.scrollIntoView({ behavior: 'smooth' });
    }
</script>
  
  <div class="box-border flex relative flex-col shrink-0 w-screen bg-orange-100 ml-[calc(50%_-_50vw)]">
    <header class="fixed-height">
    <nav class="box-border flex sticky flex-col shrink-0 w-screen h-screen ml-[calc(50%_-_50vw)]">
      <div class="flex gap-5 max-md:flex-col max-md:gap-0 max-md:">
        <div class="flex flex-col w-6/12 max-md:ml-0 max-md:w-full">
          <section class="box-border flex relative flex-col shrink-0 my-auto h-screen bg-white">
            <div class="box-border flex relative flex-col shrink-0 grow-0 h-[100px]">
              <div class="box-border flex relative flex-col shrink-0 m-auto">
                <div class="flex gap-5 max-md:flex-col max-md:gap-0 max-md:">
                  <div class="flex flex-col w-[25%] max-md:ml-0 max-md:w-full">
                    <a class="box-border relative shrink-0 px-6 py-4 my-2.5 text-center rounded appearance-none cursor-pointer text-[black]" data-el="button-1" tabindex="0" href="#about" on:click={(e) => scrollTo(e, 'about')}>about</a>
                  </div>
                  <div class="flex flex-col ml-5 w-[25%] max-md:ml-0 max-md:w-full">
                    <a class="box-border relative shrink-0 px-6 py-4 my-2.5 text-center rounded appearance-none cursor-pointer text-[black]" data-el="button-2" tabindex="0" href="#resume" on:click={(e) => scrollTo(e, 'resume')}>resume</a>
                  </div>
                  <div class="flex flex-col ml-5 w-[25%] max-md:ml-0 max-md:w-full">
                    <a class="box-border relative shrink-0 px-6 py-4 my-2.5 text-center rounded appearance-none cursor-pointer text-[black]" data-el="button-3" tabindex="0" href="#projects" on:click={(e) => scrollTo(e, 'projects')}>projects</a>
                  </div>
                  <div class="flex flex-col ml-5 w-[25%] max-md:ml-0 max-md:w-full">
                    <a class="box-border relative shrink-0 px-6 py-4 my-2.5 text-center rounded appearance-none cursor-pointer text-[black]" data-el="button-4" tabindex="0" href="#contact" on:click={(e) => scrollTo(e, 'contact')}>contact</a>
                  </div>
                </div>
              </div>
            </div>
            <div class="box-border relative py-2.5 m-auto h-auto">
              <h1 class="text-8xl font-bold">Roman Moreno Jr</h1>
              <h2 class="text-4xl font-normal">Aspiring Software Developer</h2>
            </div>
          </section>
        </div>
        <aside class="flex flex-col mr-5 w-6/12 max-md:ml-0 max-md:w-full">
          <button class="box-border relative shrink-0 self-center px-6 py-4 mt-5 mr-5 ml-auto w-auto text-center rounded appearance-none cursor-pointer bg-[black] text-[white]" data-el="button-4" tabindex="0" on:click={downloadResume}>Download Resume</button>
          <img loading="lazy" src="/files/placeholder.png" alt="A Cool Pic" class="box-border object-cover overflow-hidden shrink-0 m-auto w-full aspect-[1.42] min-h-[20px] min-w-[20px"/>
        </aside>
      </div>
     </nav>
  </header>
  </div>

  <section id="about" class="box-border flex relative flex-col shrink-0 my-auto h-screen bg-white">
    <h1 class="self-center">This is the about section</h1>
  </section>
  <section id="resume" class="box-border flex relative flex-col shrink-0 my-auto h-screen bg-white">
    <h1>This is the resume section</h1>
  </section>
  <section id="projects" class="box-border flex relative flex-col shrink-0 my-auto h-screen bg-white">
    <h1>This is the projects section</h1>
  </section>
  <section id="contact" class="box-border flex relative flex-col shrink-0 my-auto h-screen bg-white">
    <h1>This is the contact section</h1>
  </section>