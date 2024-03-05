<script>
    let images = [
      { src: 'icons/MediaNaranja.png', 
        title: 'Media Naranja Speed Dating', 
        description: `Speed dating web application that seamlessly combines React
                      for the dynamic user interface and Supabase for a backend infrastructure.
                      The heart of the system lies in the admin dashboard, offering administrators
                      the power to effortlessly create and manage events. Leveraging Supabase\'s
                      secure authentication, the application ensures airtight access control.
                      Real-time updates keep administrators informed and in control. For participants,
                      our backend utilizes Supabase\'s database to intelligently match individuals
                      based on gender, creating pairs with unique session tokens. Participants can
                      conveniently scan QR codes to connect with their matched pairs. The entire system '
                      is designed with responsiveness in mind, ensuring a seamless experience 
                      across various devices.`
      },
      //
      { src: 'icons/spotify.png', 
        title: 'Spotify Widget', 
        description: `This application, built with React in the frontend and Go in the backend, 
                      allows users to authenticate with Spotify, view their playlists, 
                      and access information about artists, and genres based on their playlists.
                      The backend interacts with both the frontend and the Spotify API, and it
                      includes a SQLite server for storing user sessions.`

      },
      //
      { src: 'icons/discord.png', 
        title: 'Lucien Bot', 
        description: `Discord bot developed in python that demonstrates a simple 
                      addition command that can add two numbers or concatenate two strings
                      together, whether they are provided as digits or strings. This showcases
                      how the bot can perform basic calculations. The bot uses the
                      discord.ext.commands framework to handle user-defined commands easily!`
      },
    ]; 
    
</script>

<form>
    <ul class="image-container snap-x snap-mandatory bg-white">
      {#each images as { src, description, title }}
        <li class="flex flex-col items-center justify-center m-10 shrink-0 snap-center">
          <img src={src} alt={description} class="image" height="200" width="500">
        </li>
        <li class="flex flex-col items-center justify-center m-10 shrink-0 snap-center">
            <h1 style="color:black" class="title">{title}</h1>
            <p style="color:black" class="description">{description}</p>
        </li>
      {/each}
    </ul>
  </form>
  
  
<style>
    .image-container {
        display: flex;
        overflow-x: auto;
        gap: 20px;
    }

    .image-container li {
    display: flex;
    justify-content: center;
    margin: 10px;
    flex-grow: 0;
    scroll-snap-align: center;
    align-items: center;
  }
    
    .image {
        max-width: 100%;
        object-fit: contain;
    }

    .description {
    font-size: 14px;
    color: #333;
    margin-top: 10px;
    white-space: pre-line;
  }
</style>