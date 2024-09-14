<template>
  <section>
    <div>

      <div class="user-data">
        <img :src="user.profileImage" alt="dp" />
        <h4 class="title is-4">{{ user.name }}</h4>

        <p>{{ user.description }}</p>


      </div>

      <div class="fixed-grid mt-5 has-1-cols-mobile has-1-col-tablet has-4-cols-desktop">
        <div class="grid">

          <div class="cell" v-for="(key, _) in keys">
            <div class="card">
              <header class="card-header">
                <p class="card-header-title">{{ key.name }}</p>
                <button class="card-header-icon" aria-label="more options">
                  <span class="icon">
                    <i class="fas fa-angle-down" aria-hidden="true"></i>
                  </span>
                </button>
              </header>
              <div class="card-content">
                <div class="content">
                  {{ key.description }}
                  <!-- <time datetime="2016-1-1">11:09 PM - 1 Jan 2016</time> -->
                </div>
              </div>
              <footer class="card-footer">
                <a href="#" class="card-footer-item">Download</a>
                <a href="#" class="card-footer-item">Copy</a>
              </footer>
            </div>
          </div>

        </div>
      </div>
    </div>
  </section>


</template>

<script setup lang="ts">
const user = {
  name: "Javier Parada",
  profileImage: "https://avatars.githubusercontent.com/u/19194763?v=4",
  description: "I'm a software engineer and a full-stack developer. I love to build web applications and learn new technologies."
}
const keys = [
  { id: "1234", name: "patata.key", description: "sd aknlwqekdbwq lkjdbq wlkd bwlqkbd qlkwdbwqlkd bwlqkdbq lwkdbqlwkd bqlw kdb w klqbdl kwbdlkqwb kldbq wklb" },
  { id: "1234", name: "patata.key", description: "sd aknlwqekdbwq lkjdbqkldbq wklb" },
  { id: "1234", name: "patata.key", description: "sd aknlwqekdbwq lkjdbq wlkd bwlqkbd qlkwdbwqlkd bwlqkdbq lwkdbqlwkd bqlw kdb w klqbdl kwbdlkqwb kldbq wklb cew cw cwe cwec wec wec wec wec wec wec wc " },
  { id: "1234", name: "patata.key", description: "sd aknlwqekdbwq lkjdbq wlk lwkdbqlwkd bqlw kdb w klqbdl kwbdlkqwb kldbq wklb" },
  { id: "1234", name: "patata.key", description: "sd aknlwqekdbwq lkjdbq wlkd bwlqkbd qlkwdbwqlkd bwlqkdbq lwkdbqlwkd bqlw kdb w klqbdl kwbdlkqwb kldbq wklb" },
  { id: "1234", name: "patata.key", description: "sd aknlwqekdbwq lkjdbq wlkd= kdb w klqbdl kwbdlkqwb kldbq wklb" },
  { id: "1234", name: "patata.key", description: "sd aknlwqekdbwq lkjdbq wlkd bwlqkbd qlkwdbwqlkd bwlqkdbq lwkdbqlwkd bqlw kdb w klqbdl kwbdlkqwb kldbq wklb" },
  { id: "1234", name: "patata.key", description: "sd aknlwqekdbwq lkjdbq wlkd bwlqkbd qlkwdbwqlkd bwlqkdbq lwkdbqlwkd bqlw kdb w klqbdlq lwkdbqlwkd bqlw kdb w klqbdl kwbdlkqwb kldbq wklb" },
  { id: "1234", name: "patata.key", description: "sd aknlwqekdbwq lkjdbq wlkd bwlqkbd qlkwdbwqlkd bwlqkdbq lwkdbqlwkd bqlw kdb w klqbdl kwbdlkqwb kldbq wklb" }
]
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  font-family: 'Poppins', sans-serif;
}

body {
  height: 100vh;
  position: relative;
  display: flex;
  flex-direction: column;
  background-color: #fefefe;
}

body>img {
  object-fit: cover;
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
}

h4 {
  margin-top: 0.3em;
}

section {
  display: grid;
  place-items: center;
  position: absolute;
  inset: 0;
  overflow-y: scroll;
}

section>div {
  width: 100%;
  max-width: 80%;
}

section div img {
  width: 150px;
  aspect-ratio: 1;
  border-radius: 50%;
}

.user-data {
  margin-top: 2em;
  margin-bottom: 5em;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1em;
}
</style>
