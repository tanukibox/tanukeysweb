<template>
  <section>
    <div>

      <img :src="user.profileImage" alt="dp" />
      <h4 class="title is-4">{{ user.name }}</h4>

      <p>{{ user.description }}</p>



    </div>
  </section>


</template>

<script setup lang="ts">
  const user = {
    name: "Javier Parada",
    profileImage: "https://avatars.githubusercontent.com/u/19194763?v=4",
    description: "I'm a software engineer and a full-stack developer. I love to build web applications and learn new technologies."
  }
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
  background-color: #0f172a;
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

section div {
  display: flex;
  flex-direction: column;
  gap: 10px;
  width: 100%;
  max-width: 600px;
  margin: 0 auto;
  padding: 10px;
  justify-content: center;
  align-items: center;
}

section>div {
  padding: 100px 10px;
}

section div img {
  width: 150px;
  aspect-ratio: 1;
  border-radius: 50%;

}
</style>
