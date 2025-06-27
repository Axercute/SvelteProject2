<script>
    import {goto} from"$app/navigation"
</script>
    <div class="homepage">
      <header class="hero">
        <h1>🎤 Welcome to Axercute Your Voice</h1>
        <p>Discover, Support & Sing Along with Your Favorite Artists</p>
      </header>

      <section class="features">
        <div class="feature-card">
          <h2>🎶 Find Song Lyrics</h2>
          <p>
            Can’t remember that one lyric? We’ve got you covered. Search for
            song lyrics by title and artist and sing along with ease.
          </p>
          <button
            onclick={() => {
              goto("/songSearch");
            }}
          >
            Search for my Song
          </button>
        </div>

        <div class="feature-card">
          <h2>🔍 Search Singers</h2>
          <p>
            Explore a growing directory of talented singers and buskers from
            around the world. Whether they’re performing on the street or
            online, you can easily find them by name, genre, or popularity.
          </p>
          <button
            onclick={() => {
              goto("/singerSearch");
            }}
          >
            Search for my Singer
          </button>
        </div>

        <div class="feature-card">
          <h2>🎙️ Interested to be a Singer?</h2>
          <p>
            Sign in and become a singer yourself! Registration is free for the
            first 100 customers.
          </p>
          <button onclick={() => goto("/singerLogin")}>
            Become a Singer
          </button>
        </div>
      </section>

      <footer class="footer">
        <p>© 2025 StreetStage. Built with ❤️ for music lovers everywhere.</p>
      </footer>
    </div>


    <style>
        /* HomePage.css */

.homepage {
  font-family: Arial, sans-serif;
  background-color: #f8f8f8;
  min-height: 100vh;
}

.hero {
  text-align: center;
  background: linear-gradient(135deg, #7b4397, #dc2430);
  color: white;
  padding: 60px 20px;
}

.features {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 20px;
  padding: 40px 20px;
}

.feature-card {
  background-color: white;
  border-radius: 12px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  width: 300px;
  padding: 30px 20px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  text-align: center;
}

.feature-card h2 {
  margin-bottom: 15px;
  font-size: 1.5rem;
}

.feature-card p {
  margin-bottom: 20px;
  font-size: 1rem;
  line-height: 1.4;
}

.feature-card button {
  margin-top: auto;
  padding: 10px 20px;
  background-color: #ff5763;
  color: white;
  border: none;
  border-radius: 6px;
  font-size: 1rem;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.feature-card button:hover {
  background-color: #a31b24;
}

.footer {
  text-align: center;
  padding: 20px;
  background-color: #222;
  color: #ddd;
  margin-top: 40px;
}

    </style>