<template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/portfolio">Portfolio</router-link> |
    <router-link to="/about">About</router-link>
  </nav>
  <router-view />
</template>

<style>
#app {
  font-family:Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #126dc8;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #126dc8;
}

nav a.router-link-exact-active {
  color: #eb5757;
}
</style>
