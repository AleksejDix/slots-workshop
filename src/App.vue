<template>
  <div class="app">
    <nav class="nav">
      <router-link to="/">Home</router-link>
      <router-link
        v-for="(n, index) in 11"
        :key="n"
        :to="{
          name: 'lesson-id',
          params: {
            id: index
          }
        }"
        >Lesson {{ index }}</router-link
      >
    </nav>
    <main class="main">
      <div class="container">
        <router-view />
      </div>
    </main>
  </div>
</template>

<style>
html {
  height: 100%;
  padding: 0;
  margin: 0;
}
body {
  min-height: 100%;
  height: 100%;
  padding: 0;
  margin: 0;
}
.app {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica,
    Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol";

  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  height: 100%;
  background: #e3e3e3;
  display: flex;
}

.owl-y > * + * {
  margin-top: 1rem;
}
.nav {
  padding: 2rem;
  background: #f5f5f5;
}

.nav a {
  font-weight: bold;
  color: #2c3e50;
  display: block;
}

.nav a.router-link-exact-active {
  color: #41b883;
}

.heroicon-ui {
  fill: currentColor;
}

.main {
  flex: 1;
}
.container {
  padding: 2rem;
  max-width: 620px;
  padding: 1rem;
  width: 100%;
  margin: 0 auto;
}

code {
  background-color: lightgreen;
  color: green;
  font-size: 1.5rem;
  padding: 0 0.5rem;
  border-radius: 0.5rem;
  font-weight: bold;
}
</style>
