<template>
  <img id="logow" alt="Vue logo" src="./assets/wwwLogo.png">
  <div id="nav">
    <router-link to="/">Home</router-link> |
    <router-link to="/world">World</router-link>
  </div>
  <router-view/>
</template>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
#logow {
  position: absolute;
  left: 0;
  top: 0;
}
#app {
  min-height: 100vh;
  background-image: url('./assets/sky-surface.jpg');
  background-size: cover;
  background-position: center;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  font-size: 20px;
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #0df88e;
}
</style>
