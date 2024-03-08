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

<div class="box-border flex relative flex-col shrink-0 w-screen h-screen bg-white ml-[calc(50%_-_50vw)]">
  <div class="box-border flex sticky flex-col shrink-0 w-screen h-screen ml-[calc(50%_-_50vw)]">
    <div class="flex gap-5 max-md:flex-col max-md:gap-0">
      <div class="flex flex-col w-6/12 max-md:ml-0 max-md:w-full h-screen">
        <div class="box-border flex relative flex-col shrink-0 my-auto min-h-screen bg-white">
          <div class="box-border flex relative flex-col shrink-0 grow-0 h-[100px]">
            <div class="box-border flex relative flex-col shrink-0 m-auto">
              <div class="flex gap-5 max-md:flex-col max-md:gap-0">
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
          <div class="flex flex-col box-border py-2.5 m-auto h-screen self-center justify-center">
            <h1 class="text-8xl font-bold">Roman Moreno Jr</h1>
            <h2 class="text-4xl font-normal">Aspiring Software Developer</h2>
          </div>
          <section id="about" class="box-border flex relative flex-col shrink-0 my-auto h-screen bg-white self-center justify-center">
            <h1 class="self-center">This is the about section</h1>
          </section>
          <section id="resume" class="box-border flex relative flex-col shrink-0 my-auto h-screen bg-white self-center justify-center">
            <h1>This is the resume section</h1>
          </section>
          <section id="projects" class="box-border flex relative flex-col shrink-0 my-auto h-screen bg-white self-center justify-center">
            <h1>This is the projects section</h1>
          </section>
          <section id="contact" class="box-border flex relative flex-col shrink-0 my-auto h-screen bg-white self-center justify-center">
            <h1>This is the contact section</h1>
          </section>
        </div>
      </div>
      <div id="right-side" class="flex flex-col w-6/12 max-md:ml-0 max-md:w-full h-screen right-0 fixed">
        <div class="box-border flex static flex-col grow shrink-0 h-auto bg-orange-100 mb-5">
          <button 
            data-el="button-4" 
            tabindex="0" 
            on:click={downloadResume}
            class="box-border relative shrink-0 self-center px-6 py-4 mt-5 mr-5 ml-auto w-auto text-center rounded appearance-none cursor-pointer bg-[black] text-[white]" >
            Download Resume
          </button>
          <img loading="lazy" src="/files/placeholder.png" alt="A Cool Pic" 
            class="box-border mx-5 object-cover overflow-hidden fixed shrink-0 my-auto self-center w-full aspect-[1.42] max-w-fit min-h-[200px] min-w-[20px] top-[200px]"
          />
        </div>
      </div>
    </div>
  </div>
</div>