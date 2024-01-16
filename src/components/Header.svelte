<script lang="ts">
  import { onMount, afterUpdate } from "svelte";

  let name = "Roman Moreno Jr";
  let isScrolled = false;

  onMount(() => {
    window.addEventListener("scroll", handleScroll);
  });

  afterUpdate(() => {
    if (isScrolled) {
      window.scrollTo(0, window.scrollY + 50);
    }
  });

  function handleScroll() {
    console.log(window.scrollY);
    isScrolled = window.scrollY > 0;
  }

  function handleClickLinkedIn() {
    console.log("LinkedIn button clicked");
    window.open("https://www.linkedin.com/in/roman-moreno-jr/", "_blank");
  }

  function handleClickGithub() {
    console.log("Github button clicked");
  }

  function handleClickEmail() {
    console.log("Email button clicked");
  }
</script>


<header
  class="flex items-center justify-between bg-blue-500 text-white text-6xl font-extrabold p-5"
  style:position={isScrolled ? "fixed" : "static"}
>
  <p class="mr-auto">{name}</p>
  <div class="flex">
    <button on:click={handleClickLinkedIn}>
      <img src ="/icons/linkedin_icon.png" alt="Twitter" class="w-12 h-12"/>
    </button>
    <button on:click={handleClickGithub}>
      <img src="/icons/github_icon.png" alt="Github" class="w-12 h-12"/>
    </button>
    <button on:click={handleClickEmail}>
      <img src="/icons/mail_icon.png" alt="Email" class="w-12 h-12"/>
    </button>
  </div>
</header>