<script>
    let images = [
      { src: 'icons/MediaNaranja.svg', description: 'Media Naranja Speed Dating' },
      { src: 'icons/spotify.png', description: 'Spotify Widget' },
      { src: 'icons/discord.png', description: 'Lucien Bot' },
    ];

    function handleClickLinkedIn() {
        console.log("LinkedIn button clicked");
        window.open("https://www.linkedin.com/in/roman-moreno-jr/", "_blank");
    }
</script>

<div class="image-container">
    {#each images as { src, description }}
        <div class="flex justify-center m-10">
            <img src={src} alt={description} class="image" height="96" width="96">
            <p>{description}</p>
        </div>
    {/each}
</div>
  
<style>
    .image-container {
        display: flex;
        overflow-x: auto;
        gap: 20px; /* Adjust the gap between images */
    }
    
    .image {
        max-width: 100%; /* Ensure images don't exceed container width */
    }
    </style>