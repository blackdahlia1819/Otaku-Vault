# Otaku-Vault
Submission for the 2024 Winter Hackathon by Codedex
Otaku Vault

Welcome to Otaku Vault, your one-stop destination for anime enthusiasts! This website is dedicated to showcasing your favorite anime series, characters, and more in a visually appealing and user-friendly manner Taking place in the late 90s. Explore the vault and immerse yourself in the world of anime!

Live Demo

Check out the live website here: https://blackdahlia1819.github.io/Otaku-Vault/

Features

Anime Showcase: Explore curated lists of popular anime series.

Responsive Design: Fully responsive website optimized for desktops, tablets, and mobile devices.

Interactive Elements: Navigate through dynamic content with ease.

Visually Appealing Layout: Designed with a clean and modern aesthetic to enhance user experience.

Screenshots

![image](https://github.com/user-attachments/assets/6de26145-cb4e-4f82-b386-6112ece58145)

![image](https://github.com/user-attachments/assets/ee093f6c-ad91-4986-84f2-7759b55fade0)

Technologies Used

HTML5: For the structure and layout of the website.

CSS3: For styling and visual design.

JavaScript: For interactivity and functionality.

Getting Started

Follow these steps to get a local copy of the project up and running:

Prerequisites

A modern web browser (e.g., Chrome, Safari, Firefox, Edge).

Installation

Clone the repository:

git clone https://github.com/blackdahlia1819/Otaku-Vault.git

Navigate to the project directory:

cd Otaku-Vault

Open the index.html file in your browser to view the site locally.

Contact

For any inquiries or feedback, feel free to reach out:

GitHub: blackdahlia1819

Email: saminyc007@gmail.com

Acknowledgments

Inspired by the passion and creativity of anime fans worldwide.

Special thanks to the anime community for their continued support and love.

This is the code...idk if you can already see it somewhere else but im extremely new to Github and web dev in general, i just started coding and web dev 4 weeks ago, ebfore that ive never been in tec at all. So please be patient and enjoy this project, also here's the code just in case♡

[Uploading index.html…]()<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Anime Collectibles Shop</title>
    <style>
      /* Global Styling */
      * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
      }

      /* Smooth Scroll */
      html {
        scroll-behavior: smooth;
      }

      /* Body & Background */
      body {
        font-family: "Comic Sans MS", sans-serif;
        color: #00ff00;
        font-size: 16px;
        text-align: center;
        background: url("background.gif") repeat;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        overflow-x: hidden;
      }

      /* Flashing text animation */
      @keyframes flashText {
        0% {
          color: #ffff00;
        }
        50% {
          color: #ff00ff;
        }
        100% {
          color: #ffff00;
        }
      }

      .flashing-text {
        font-size: 2em;
        animation: flashText 1s infinite;
      }

      /* Main window styling */
      .window {
        width: 80%;
        max-width: 1000px;
        margin: 50px auto;
        background-color: rgba(0, 0, 0, 0.85);
        border: 5px solid #00ff00;
        box-shadow: 0 0 20px rgba(0, 255, 0, 0.6);
        padding: 20px;
        border-radius: 15px;
        overflow: hidden;
        z-index: 1;
      }

      /* Title Bar */
      .window .title-bar {
        background-color: #222;
        color: #00ff00;
        padding: 10px;
        font-size: 18px;
        font-weight: bold;
        text-align: center;
        border-radius: 10px 10px 0 0;
        text-shadow: 2px 2px 5px rgba(255, 255, 255, 0.7);
      }

      /* Retro-styled buttons */
      .button {
        background-color: #ff00ff;
        color: #000;
        padding: 10px 20px;
        border: 3px solid #000;
        border-radius: 5px;
        font-size: 18px;
        text-decoration: none;
        cursor: pointer;
        font-family: "Courier New", Courier, monospace;
        margin: 5px;
        box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.5);
        text-transform: uppercase;
      }

      .button:hover {
        background-color: #00ff00;
        color: #000;
        box-shadow: 0 0 10px rgba(255, 255, 255, 0.8);
      }

      /* Table for Products */
      table {
        width: 100%;
        border-collapse: collapse;
        margin-top: 20px;
        border: 3px solid #ff00ff;
      }

      th,
      td {
        padding: 15px;
        text-align: center;
      }

      th {
        background-color: #222;
        color: #ff00ff;
        font-family: "Courier New", Courier, monospace;
        text-shadow: 1px 1px 3px rgba(255, 255, 255, 0.6);
      }

      td {
        background-color: #003300;
        color: #00ff00;
        border: 2px solid #ff00ff;
      }

      /* Sidebar navigation */
      .sidebar {
        background-color: #222;
        color: white;
        width: 250px;
        padding: 15px;
        position: fixed;
        left: 20px;
        top: 20px;
        border-radius: 15px;
        box-shadow: 0 0 20px rgba(0, 0, 0, 0.7);
        z-index: 1;
      }

      .sidebar a {
        color: white;
        text-decoration: none;
        display: block;
        padding: 10px;
        margin: 5px 0;
        font-size: 20px;
        background-color: #000;
        border-radius: 10px;
        box-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
      }

      .sidebar a:hover {
        background-color: #ff00ff;
        color: #000;
      }

      /* Footer */
      footer {
        background-color: #222;
        color: white;
        padding: 10px;
        font-size: 14px;
        text-align: center;
        position: fixed;
        bottom: 0;
        width: 100%;
        z-index: 1;
      }

      /* About Section */
      #about {
        background-color: #222;
        color: #00ff00;
        padding: 20px;
        border-radius: 10px;
        margin-top: 20px;
        box-shadow: 0 0 20px rgba(0, 255, 0, 0.5);
      }

      .about-image {
        width: 150px;
        margin-right: 15px;
        border-radius: 5px;
        box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.5);
      }

      .about-text {
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 15px;
      }

      /* GIF Section (Anime GIFs) */
      .gif-container {
        display: flex;
        justify-content: center;
        gap: 10px;
        margin-top: 20px;
      }

      img {
        width: 100%;
        height: auto;
        border: 3px solid #ff00ff;
      }

      /* Card Section */
      .card-category {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        gap: 20px;
        margin-top: 20px;
      }

      .card {
        background-color: #222;
        padding: 15px;
        border: 3px solid #ff00ff;
        border-radius: 10px;
        width: 200px;
        text-align: center;
      }

      .card img {
        width: 100%;
        height: auto;
        border: 3px solid #ff00ff;
        border-radius: 5px;
        box-shadow: 0 0 10px rgba(255, 255, 255, 0.8);
      }

      .card h4 {
        color: #ff00ff;
        font-size: 1.2em;
        margin-top: 10px;
      }

      .card span {
        display: block;
        margin-top: 5px;
        color: #00ff00;
      }
    </style>
  </head>
  <body>
    <!-- Sidebar Navigation -->
    <div class="sidebar">
      <h3>Menu</h3>
      <a href="#">Home</a>
      <!-- Link back to the main page -->
      <a href="#about">About Us</a>
      <a href="#pokemon">Pokemon Cards</a>
    </div>

    <!-- Background Music -->
    <audio autoplay loop id="background-audio">
      <source src="song.mp3" type="audio/mp3" />
      Your browser does not support the audio element.
    </audio>

    <!-- Main Content Window -->
    <div class="window">
      <!-- Audio button -->
      <button id="play-button" class="button">Play Audio</button>

      <!-- Title Bar -->
      <div class="title-bar">
        <span>Anime Collectibles Shop</span>
      </div>

      <!-- Marquee with Flashing Text -->
      <marquee>** Welcome to the Ultimate Collectibles Store! **</marquee>
      <h2 class="flashing-text">
        Anime Figurines, Beyblades, Trading Cards and More!
      </h2>

      <!-- Product Listings -->
      <div id="figurines">
        <h3>Anime Figurines</h3>
        <table>
          <tr>
            <th>Product</th>
            <th>Price</th>
            <th>Buy Now</th>
          </tr>
          <tr>
            <td>Dragon Ball Z Goku</td>
            <td>$15.99</td>
            <td><a href="#" class="button">Buy</a></td>
          </tr>
          <tr>
            <td>Naruto Uzumaki</td>
            <td>$15.99</td>
            <td><a href="#" class="button">Buy</a></td>
          </tr>
          <tr>
            <td>Sailor Moon</td>
            <td>$19.99</td>
            <td><a href="#" class="button">Buy</a></td>
          </tr>
        </table>
      </div>

      <div id="beyblades">
        <h3>Beyblades</h3>
        <table>
          <tr>
            <th>Product</th>
            <th>Price</th>
            <th>Buy</th>
          </tr>

          <tr>
            <td>Dranzer</td>
            <td>$10.99</td>
            <td><a href="#" class="button">Buy</a></td>
          </tr>
          <tr>
            <td>Dragoon</td>
            <td>$13.99</td>
            <td><a href="#" class="button">Buy</a></td>
          </tr>
          <tr>
            <td>Gaia Dragoon</td>
            <td>$15.99</td>
            <td><a href="#" class="button">Buy</a></td>
          </tr>
        </table>
      </div>

      <div id="trading-cards">
        <h3>Trading Cards</h3>
        <table>
          <tr>
            <th>Product</th>
            <th>Price</th>
            <th>Buy Now</th>
          </tr>
          <tr>
            <td>Yu-Gi-Oh! Dark Magician Girl</td>
            <td>$20.99</td>
            <td><a href="#" class="button">Buy</a></td>
          </tr>
          <tr>
            <td>Yu-Gi-Oh! Blue Eyes White Dragon</td>
            <td>$20.99</td>
            <td><a href="#" class="button">Buy</a></td>
          </tr>
          <tr>
            <td>Yu-Gi-Oh! Scarlet Erythion</td>
            <td>$25.99</td>
            <td><a href="#" class="button">Buy</a></td>
          </tr>
          <tr>
            <td>Pokémon Rare Charizard</td>
            <td>$15.99</td>
            <td><a href="#" class="button">Buy</a></td>
          </tr>
          <tr>
            <td>Common Pokémon Pikachu</td>
            <td>$5.99</td>
            <td><a href="#" class="button">Buy</a></td>
          </tr>
          <tr>
            <td>Ultra Rare Blastoise</td>
            <td>$20.99</td>
            <td><a href="#" class="button">Buy</a></td>
          </tr>
          <tr>
            <td>Legendary Mewtwo</td>
            <td>$50.99</td>
            <td><a href="#" class="button">Buy</a></td>
          </tr>
        </table>
      </div>

      <!-- About Section -->
      <div id="about">
        <h1>About Us</h1>
        <div class="about-text">
          <img
            class="about-image"
            src="https://scontent-lga3-1.xx.fbcdn.net/v/t39.30808-6/301941753_216749454012593_5577290368050279691_n.jpg?_nc_cat=108&ccb=1-7&_nc_sid=833d8c&_nc_ohc=fimE1-Ba-pQQ7kNvgGI3MNK&_nc_zt=23&_nc_ht=scontent-lga3-1.xx&_nc_gid=A4ylgpAM_dBONzhFAFBvGjh&oh=00_AYBhGYUDW_SLWU521Yu35LHagtdhZ5HSKmaQkiuxDF8TRA&oe=6762DD2E"
            alt="Figure"
          />
          <p>
            We are an anime and collectible store, offering the best selection
            of cool and cheap figurines, Beyblades, and trading cards. Dive into
            this site and collect the best of the best!
          </p>
        </div>
      </div>

      <!-- GIF Section (Anime GIFs) -->
      <div class="gif-container">
        <img
          src="https://media4.giphy.com/media/v1.Y2lkPTc5MGI3NjExdGduNHd3bjR1ZWpud2l0M3Vjc3pzODF5NjcxemNpYnltd2pzdG9tNSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/nBHnyQePKnES4/giphy.webp"
          alt="Pokémon GIF"
        />
        <img
          src="https://img1.picmix.com/output/pic/normal/5/8/4/6/11956485_ec793.gif"
          alt="Beyblade GIF"
        />
      </div>
    </div>

    <!-- Main Content Window -->
    <div class="window">
      <!-- Title Bar -->
      <div class="title-bar">
        <span>Pokémon Cards</span>
      </div>

      <h2 class="flashing-text">Collect the Best Pokémon Cards!</h2>

      <!-- Pokémon Card Categories -->
      <div class="card-category">
        <div class="card common">
          <img src="https://i.redd.it/jn9chock3yr71.gif" alt="Common Pikachu" />
          <h4>Common Pikachu</h4>
          <span>$5.99</span>
        </div>

        <div class="card rare">
          <img
            src="https://www.pokemon.com/static-assets/content-assets/cms2/img/trading-card-game/series/incrementals/2024/charizard-ex-super-premium-collection/inline/SVP_EN_161.gif"
            alt="Rare Charizard"
          />
          <h4>Rare Charizard</h4>
          <span>$15.99</span>
        </div>

        <div class="card ultra-rare">
          <img
            src="https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/3777a232-f379-448a-bc55-19243fc4fabe/dfsx2gb-aa0a93c1-485d-495c-a344-f65e90b08cc9.gif?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7InBhdGgiOiJcL2ZcLzM3NzdhMjMyLWYzNzktNDQ4YS1iYzU1LTE5MjQzZmM0ZmFiZVwvZGZzeDJnYi1hYTBhOTNjMS00ODVkLTQ5NWMtYTM0NC1mNjVlOTBiMDhjYzkuZ2lmIn1dXSwiYXVkIjpbInVybjpzZXJ2aWNlOmZpbGUuZG93bmxvYWQiXX0.ZrIe0DlHGJh3KfHRtUqCaleS3GdaoaUcEqpcr0ShoEU"
            alt="Ultra Rare Blastoise"
          />
          <h4>Ultra Rare Blastoise</h4>
          <span>$20.99</span>
        </div>

        <div class="card legendary">
          <img
            src="https://i.pinimg.com/originals/42/70/e3/4270e3fdc89aab4db2d1e52315f20537.gif"
            alt="Legendary Mewtwo"
          />
          <h4>Legendary Mewtwo</h4>
          <span>$50.99</span>
        </div>
      </div>
    </div>

    <!-- Main Content Window -->
    <div class="window">
      <!-- Title Bar -->
      <div class="title-bar">
        <span>Yu-Gi-Oh! Cards</span>
      </div>

      <h2 class="flashing-text">Collect the Best Yu-Gi-Oh! Cards!</h2>

      <!-- Yu-Gi-Oh! Card Categories -->
      <div class="card-category">
        <div class="card common">
          <img
            src="https://preview.redd.it/tyf32lswemp71.gif?width=438&format=mp4&s=f9a99f3ada9d3f96fe2769e52ed2012033ddf95f"
            alt="Common Pikachu"
          />
          <h4>Dark Magician Girl</h4>
          <span>$20.99</span>
        </div>

        <div class="card ultra-rare">
          <img
            src="https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/97cabb08-cc9e-454a-90d6-a2fd9cec595a/d9rzmvt-14523095-4945-47d0-ac86-70a0c0d88f3d.gif?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7InBhdGgiOiJcL2ZcLzk3Y2FiYjA4LWNjOWUtNDU0YS05MGQ2LWEyZmQ5Y2VjNTk1YVwvZDlyem12dC0xNDUyMzA5NS00OTQ1LTQ3ZDAtYWM4Ni03MGEwYzBkODhmM2QuZ2lmIn1dXSwiYXVkIjpbInVybjpzZXJ2aWNlOmZpbGUuZG93bmxvYWQiXX0.fjORqJQTiqeLvje1YLkfEOTBdoQfFO9T-zbCrTNsGmg"
            alt="Ultra Rare Blastoise"
          />
          <h4>Blue Eyes White Dragon</h4>
          <span>$20.99</span>
        </div>

        <div class="card legendary">
          <img
            src="https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/86f0b4fc-27ee-4f75-89d0-498bc898d4ab/dgxwsg2-df4a000a-c092-46d1-b327-0ac99992b87b.gif?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7InBhdGgiOiJcL2ZcLzg2ZjBiNGZjLTI3ZWUtNGY3NS04OWQwLTQ5OGJjODk4ZDRhYlwvZGd4d3NnMi1kZjRhMDAwYS1jMDkyLTQ2ZDEtYjMyNy0wYWM5OTk5MmI4N2IuZ2lmIn1dXSwiYXVkIjpbInVybjpzZXJ2aWNlOmZpbGUuZG93bmxvYWQiXX0.isa0KpOMXTrpZcJ1bxFrcrYFYWL8ZFrnNa_mbIsWwjU"
            alt="Legendary Mewtwo"
          />
          <h4>Scarlet Erythion</h4>
          <span>$25.99</span>
        </div>
      </div>
    </div>

    <!-- Main Content Window -->
    <div class="window">
      <!-- Title Bar -->
      <div class="title-bar">
        <span>Anime Figurines</span>
      </div>

      <h2 class="flashing-text">Collect the Best Figurines!</h2>

      <!-- Anime Figurines Categories -->
      <div class="card-category">
        <div class="card common">
          <img
            src="https://i.ebayimg.com/images/g/LRAAAOSw~TxkanmC/s-l1600.jpg"
            alt="Common Pikachu"
          />
          <h4>Dragon Ball Z Goku</h4>
          <span>$15.99</span>
        </div>

        <div class="card ultra-rare">
          <img
            src="https://i.ebayimg.com/images/g/0a8AAOSwl41nQJtg/s-l1600.png"
            alt="Ultra Rare Blastoise"
          />
          <h4>Naruto Uzumaki</h4>
          <span>$15.99</span>
        </div>

        <div class="card legendary">
          <img
            src="https://i.ebayimg.com/images/g/0EEAAOSwp0dl9o0~/s-l1600.jpg"
            alt="Legendary Mewtwo"
          />
          <h4>Sailor Moon</h4>
          <span>$19.99</span>
        </div>
      </div>
    </div>

    <!-- Main Content Window -->
    <div class="window">
      <!-- Title Bar -->
      <div class="title-bar">
        <span>Beyblades Figurines</span>
      </div>

      <h2 class="flashing-text">Collect the Best Beyblades!</h2>

      <!-- Beyblades Categories -->
      <div class="card-category">
        <div class="card common">
          <img src="https://i.redd.it/rvxhwsr6l0m61.jpg" alt="Common Dranzer" />
          <h4>Dranzer</h4>
          <span>$10.99</span>
        </div>

        <div class="card ultra-rare">
          <img
            src="https://i.ebayimg.com/images/g/VWgAAOSwnTNhZozY/s-l1600.jpg"
            alt="Ultra Rare Dragoon"
          />
          <h4>Dragoon</h4>
          <span>$13.99</span>
        </div>

        <div class="card legendary">
          <img
            src="https://i.ebayimg.com/images/g/ImAAAOSwxKJmuriL/s-l1600.jpg"
            alt="Legendary Gaia"
          />
          <h4>Gaia Dragoon</h4>
          <span>$15.99</span>
        </div>
      </div>
    </div>

    <!-- Footer -->
    <footer class="footer">
      <p>&copy; 2024 Anime Collectibles Shop. All Rights Reserved.</p>
    </footer>

    <script>
      const playButton = document.getElementById("play-button");
      const audio = document.getElementById("background-audio");
      audio.volume = 0.2;

      playButton.addEventListener("click", () => {
        if (audio.paused) {
          audio.play();
          playButton.textContent = "Pause Audio";
        } else {
          audio.pause();
          playButton.textContent = "Play Audio";
        }
      });
    </script>
  </body>
</html>



