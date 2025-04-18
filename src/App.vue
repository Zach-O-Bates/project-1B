<template>
  <div class="app-container">
    <!-- Home Page -->
    <div v-if="currentPage === 'home'" class="menu-container">
      <div class="header">
        <div class="left-nav">
          <span class="nav-item" @click="goTo('about')">About</span>
        </div>
        <span class="nav-item right" @click="goTo('developers')">Devs</span>
      </div>

      <div class="main-content">
        <button class="arrow" @click="prev">&#8592;</button>
        <div class="game-box" @click="goTo('gameDesc')">
          <div class="button-a">A</div>
          <div class="game-label">Game</div>
        </div>
        <button class="arrow" @click="next">&#8594;</button>
      </div>

      <div class="genre">
        <div>Game Genre: Action</div>
        <div class="genre-name">Developer: Lorem Ipsum</div>
      </div>
    </div>

    <!-- About Page -->
    <div v-else-if="currentPage === 'about'" class="menu-container">
      <button class="about-back-button" @click="goTo('home')">Back</button>
      <div class="about-page">
        <div class="about-title">
          <h1>About the Cabinet</h1>
        </div>

        <div class="about-description">
          <div class="about-content"> 
            Lorem ipsum dolor sit amet consectetur adipiscing elit. Quisque faucibus ex sapien vitae pellentesque sem placerat. In id cursus mi pretium tellus duis convallis. 
            Lorem ipsum dolor sit amet consectetur adipiscing elit. Sit amet consectetur adipiscing elit quisque faucibus ex. Adipiscing elit quisque faucibus ex sapien vitae pellentesque.
            Lorem ipsum dolor sit amet consectetur adipiscing elit. Sit amet consectetur adipiscing elit quisque faucibus ex. Adipiscing elit quisque faucibus ex sapien vitae pellentesque.
          </div>

          <div class="about-photo">
            <div class="game-label">Image</div>
          </div>

        </div>

        <div class="about-description">
          <div class="about-content-long"> 
            Lorem ipsum dolor sit amet consectetur adipiscing elit. Quisque faucibus ex sapien vitae pellentesque sem placerat. In id cursus mi pretium tellus duis convallis. 
            Lorem ipsum dolor sit amet consectetur adipiscing elit. Sit amet consectetur adipiscing elit quisque faucibus ex. Adipiscing elit quisque faucibus ex sapien vitae pellentesque.
            Lorem ipsum dolor sit amet consectetur adipiscing elit. Sit amet consectetur adipiscing elit quisque faucibus ex. Adipiscing elit quisque faucibus ex sapien vitae pellentesque.
            Lorem ipsum dolor sit amet consectetur adipiscing elit. Quisque faucibus ex sapien vitae pellentesque sem placerat. In id cursus mi pretium tellus duis convallis. 
          </div>
        </div>

        <div class="about-description">

          <div class="about-photo">
            <div class="game-label">Image</div>
          </div>

          <div class="about-content"> 
            Lorem ipsum dolor sit amet consectetur adipiscing elit. Quisque faucibus ex sapien vitae pellentesque sem placerat. In id cursus mi pretium tellus duis convallis. 
            Lorem ipsum dolor sit amet consectetur adipiscing elit. Sit amet consectetur adipiscing elit quisque faucibus ex. Adipiscing elit quisque faucibus ex sapien vitae pellentesque.
            Lorem ipsum dolor sit amet consectetur adipiscing elit. Sit amet consectetur adipiscing elit quisque faucibus ex. Adipiscing elit quisque faucibus ex sapien vitae pellentesque.
          </div>

        </div>
        <button class="about-back-button" @click="goTo('home')">Back</button>



      </div>
    </div>

    <!-- Game Description -->

    <div v-else-if="currentPage === 'gameDesc'" class="menu-container">
      <button class="back-button" @click="goTo('home')">Back</button>

      <div class="text-center">
        <h3>Game Name</h3>
      </div>

      <div class="main-content">
        <div class="game-left">
          <div class="game-label">Game Image</div>
        </div>
        <div class="game-center">
          <div class="game-label">Game Image</div>
        </div>
        <div class="game-right">
          <div class="game-label">Game Image</div>
        </div>
      </div>

      <div>
        Lorem ipsum dolor sit amet consectetur adipiscing elit. Sit amet consectetur adipiscing elit quisque faucibus ex. Adipiscing elit quisque faucibus ex sapien vitae pellentesque.
      </div>

      <button class="play">Play</button>
    </div>

    <!-- Developers Page -->
    <div v-else-if="currentPage === 'developers'" class="content-card">
      <div class="small-rectangles">
        <div class="small-rectangle">
          <img src="/public/Travis.jpg" class="dev-img">
          <p class="dev-desc">Travis: A passionate and creative game developer</p>
          <img src="/public/QR1.png" class="dev-img">
        </div>
        <div class="small-rectangle">
          <img src="/public/BuffTravis.jpg" class="dev-img">
          <p class="dev-desc">Buff Travis: Travis but so buff it looks fake</p>
          <img src="/public/QR2.png" class="dev-img">
        </div>
        <div class="small-rectangle">
          <img src="/public/image-2.png" class="dev-img">
          <p class="dev-desc">Saaf Sivart: The evil version of Travis</p>
          <img src="/public/QR3.png" class="dev-img">
        </div>
        <button class="back-button" @click="goTo('home')">Back</button>
      </div>
      
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      currentPage: 'home'
    }
  },
  methods: {
    goTo(page) {
      this.currentPage = page;
    },
    prev() {
      // prev game logic
    },
    next() {
      // next game logic
    }
  }
}
</script>

<style>
body, html, #app {
  margin: 0;
  padding: 0;
  height: 100%;
}

.app-container {
  height: 100vh;
  width: 100vw;
  display: flex;
  justify-content: center;
  align-items: center;
  background: linear-gradient(to bottom, #1E1E1E, #251C53);
  color: white;
  text-align: center;
  font-family: sans-serif;
}

.menu-container {
  padding: 20px;
}

.header {
  display: flex;
  justify-content: space-between;
  margin: 50px 0;
  color: #7572a1;
  font-size: 1.2em;
}

.left-nav {
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.nav-item {
  cursor: pointer;
}

.main-content {
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 100px 0;
}

.arrow {
  background: none;
  border: none;
  color: #c51878;
  font-size: 2em;
  cursor: pointer;
}

.game-box {
  background: #dcdcdc;
  color: black;
  padding: 20px;
  margin: 0 20px;
  width: 300px;
  height: 300px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  cursor: pointer;
}

.button-a {
  background: #3a2c91;
  border-radius: 50%;
  color: white;
  width: 30px;
  height: 30px;
  display: flex;
  justify-content: center;
  align-items: center;
  margin-bottom: 10px;
}

.genre {
  font-size: 1.5em;
}

.genre-name {
  font-size: 2em;
  font-weight: bold;
  margin-top: 10px;
}

.back-button {
  margin-bottom: 20px;
  padding: 10px 20px;
  background-color: #88aaff;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  color: #1E1E1E;
}

/* Game Boxes */

.game-left, .game-center, .game-right {
  background: #dcdcdc;
  color: black;
  padding: 20px;
  margin: 0 20px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

.game-left, .game-right {
  width: 75px;
  height: 25px;
}

.game-center {
  width: 200px;
  height: 100px;
}



.play {
  background: #C42577;
  color: white;
  font-size: xx-large;
  width: 150px;
  height: 75px;
  border: none;
  margin-top: 20px;
  cursor: pointer;
}

/* Developer Page */

.content-card {
  background-color: #40519D;
  padding: 2rem;
  border-radius: 1rem;
  height: 550px;
  width: 800px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.small-rectangles {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  width: 100%;
  align-items: center;
  margin-top: 1rem;
}

.small-rectangle {
  width: 1250px;
  min-height: 150px;
  background-color: #1E1E1E;
  border-radius: 0.5rem;
  display: flex;
  align-items: center;
  justify-content: space-around;
  padding: 1rem;
  gap: 1rem;
}

.small-rectangle {
  width: 600px;
  min-height: 150px;
  background-color: #1E1E1E;
  border-radius: 0.5rem;
  display: flex;
  align-items: center;
  justify-content: space-around;
  padding: 1rem;
  gap: 1rem;
}

.dev-img {
  width: 100px;
  height: 100px;
  object-fit: cover;
  border-radius: 0.5rem;
}

.dev-desc {
  flex: 1;
  text-align: center;
}

/* About Page */

.about-page {
  align-items: center;
}

.about-back-button {
  margin-bottom: 20px;
  padding: 10px 20px;
  background-color: #88aaff;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  color: #1E1E1E;
  
}

.about-content {
  width: 500px;
  height: 300px
}

.about-description {
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 20px ;
}

.about-photo {
  background: #dcdcdc;
  color: black;
  padding: 20px;
  margin: 20px;
  width:  300px;
  height: 300px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  cursor: pointer;
}

.about-content, .about-photo {
  padding: 20px;
  margin: 0 20px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

.about-content-long {
  width: 800px;
  height: 150px
}

</style>