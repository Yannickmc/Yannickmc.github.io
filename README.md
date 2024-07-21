<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Aliplayer</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      margin: 0;
      padding: 0;
      background-color: #271b51f7;
      color: white; /* Text color */
    }

    h1 {
      margin-top: 10px;
    }

    #playlist {
            list-style: none;
            padding: 0;
            display: flex;
            flex-direction: column;
            align-items: flex-start; /* Align to the left */
            max-height: 630px; /* Set a maximum height */
            overflow-y: auto; /* Enable vertical scroll */
        }

        #playlist li {
            margin: 10px;
            padding: 10px;
            border: 1px solid #463090;
            border-radius: 5px;
            background-color: #463090;
            width: 370px;
            cursor: pointer;
            transition: background-color 0.3s;
            margin-left: 10px; /* Add left margin */
        }

        #playlist li:hover {
            background-color: #36256f;  
       }



    audio {
            width: 100%;
            max-width: 400px;
            margin-top: 0px;
            background-color: #f0f0f0;
            border: 1px solid #ccc;
            border-radius: 5px;
            outline: none;
        }
        
        
        audio::-webkit-media-controls {
           Download-display: none;
        }
        #currentSongIndex {
            margin-top: 10px;
    }
  </style>
</head>
<body>
  <h1>Aliplayer</h1>
  
  <ul id="playlist">
    <li data-src="https://files.thenaatsharif.com/downloads/maher-zain/huwa-ahmadun.mp3">huwa-ahmadun.mp3</li>
    <li data-src="https://files.thenaatsharif.com/downloads/maher-zain/I-am-alive.mp3">I'mlive</li>
   <li data-src="https://naijafinix.com/wp-content/uploads/2021/11/Maher-Zain-Hubb-Ennabi-Loving-the-Prophet-via-Naijafinix.com_.mp3">hubb ennabi-maher</li>
   <li data-src="https://www.360hausa.com.ng/wp-content/uploads/2022/04/Ya-Nabi-Salam-Alaika-Arabic-360Hausa.Com-Maher-Zain.mp3">ya-nabi-salam-alayka.mp3</li>
   <li data-src="https://files.thenaatsharif.com/downloads/maher-zain/ramadan-ramazan.mp3">Ramadan.mp3</li>
   <li data-src="https://files.thenaatsharif.com/downloads/maher-zain/huwa-alquran.mp3">huwa-alquran.mp3</li>
   <li data-src="https://files.thenaatsharif.com/downloads/maher-zain/mawlaya(arabic).mp3">mawlayasalli.mp3</li>
   <li data-src="https://djyoungster.net/music/128/LaTest%20Hindi/One%20-%20(Maher%20Zain)/Allah%20Ya%20Moulana-Maher%20Zain(One).mp3">Allah ya moulana.mp3</li>
   <li data-src="https://naijafinix.com/wp-content/uploads/2021/11/Maher-Zain-Mustafa-Ceceli-Bika-Moulhimi-via-Naijafinix.com_.mp3">Bika moulhimi.mp3</li>
   <li data-src="https://files.gospeljingle.com/uploads/music/2023/03/Maher_Zain_-_Rahmatun_Lil_Alameen.mp3">Rahmatun_Lil_Alameen.mp3</li>
   <li data-src="https://naijafinix.com/wp-content/uploads/2021/11/Maher-Zain-Radhitu-Billahi-Rabba-English-Version-via-Naijafinix.com_.mp3">Radhitu Billahi Rabba.mp3</li>
  </ul>

  <audio id="audioPlayer" controls>
    Your browser does not support the audio element.
  </audio>

  <script>
    const playlist = document.getElementById('playlist');
  const audioPlayer = document.getElementById('audioPlayer');
  const playlistItems = playlist.getElementsByTagName('li');
  let currentSongIndex = 0;

  playlist.addEventListener('click', (event) => {
    if (event.target.tagName === 'LI') {
      const audioSource = event.target.getAttribute('data-src');
      playAudio(audioSource);
    }
  });

  audioPlayer.addEventListener('ended', () => {
    // Move to the next song in the playlist
    currentSongIndex = (currentSongIndex + 1) % playlistItems.length;
    const nextSong = playlistItems[currentSongIndex];
    const audioSource = nextSong.getAttribute('data-src');
    playAudio(audioSource);
  });

  function playAudio(source) {
    audioPlayer.src = source;
    audioPlayer.play();
  }
</script>
  </script>
</body>
</htm>
