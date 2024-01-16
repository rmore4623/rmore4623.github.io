<script lang="ts">
  let name = "Roman Moreno Jr";

  function handleClickLinkedIn() {
    console.log("LinkedIn button clicked");
    window.open("https://www.linkedin.com/in/romanmorenojr/", "_blank");
  }

  function handleClickGithub() {
    console.log("Github button clicked");
    window.open("https://github.com/rmore4623", "_blank");
  }

  function handleClickEmail() {
    console.log("Email button clicked");
  }
</script>


<header
  class="flex items-center justify-between bg-blue-500 text-white text-6xl font-extrabold p-5"
>
  <p class="mr-auto">{name}</p>
  <div class="flex">
    <button on:click={handleClickLinkedIn}>
      <img src ="/icons/linkedin_icon.png" alt="Twitter" class="w-12 h-12 mr-10"/>
    </button>
    <button on:click={handleClickGithub}>
      <img src="/icons/github_icon.png" alt="Github" class="w-12 h-12 mr-10"/>
    </button>
    <button on:click={handleClickEmail}>
      <img src="/icons/mail_icon.png" alt="Email" class="w-12 h-12 mr-10"/>
    </button>
  </div>
</header>