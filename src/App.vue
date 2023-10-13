<script setup>
import { RouterLink, RouterView } from "vue-router";
</script>

<template>
  <head>
    <link
      href="https://fonts.googleapis.com/css2?family=Josefin+Sans:wght@500&family=Yusei+Magic&display=swap"
      rel="stylesheet"
    />
  </head>
  <header>
    <div class="decor-top">
      <img src="img/plannt 1.png" class="decor dh1" />
      <img src="img/plannt 1.png" class="decor dh2" />
    </div>
    <div class="top">
      <img src="img/sunu.png" class="logo" />

      <h1 class="title">LA MAGIA</h1>

      <h3 class="sub-title">smoothie bowls</h3>
    </div>

    <div class="wrapper">
      <nav>
        <RouterLink to="/"></RouterLink>
        <RouterLink to="/about"></RouterLink>
      </nav>
    </div>
  </header>
  <main>
    <RouterView />
    <div class="decor-bottom">
      <img src="img/plannt 1.png" class="decor dh3" />

      <img src="img/plannt 1.png" class="decor dh4" />
    </div>
  </main>
</template>

<style scoped>
.logo {
  display: flex;
  left: 50px;
}
.top {
  display: flex;
  align-content: center;
  flex-direction: column;
  align-items: center;
}
.decor-top {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  width: 100%;
}
.decor {
  width: 100px;
}
.decor-bottom {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
.title {
  font-family: Yusei Magic;
  font-weight: bold;
  font-size: 45px;
}
.sub-title {
  font-family: josefin sans;
}
header {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  color: var(--white-vintage);
}
.decor-footer {
  height: 100px;
  width: 100px;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
  width: 100px;
  height: 100px;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
