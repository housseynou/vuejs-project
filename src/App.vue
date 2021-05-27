<template>
  <div id="nav">
    <main>
      <router-link to="/">Home</router-link> |
      <router-link to="/about">The World Weather</router-link>
      <div class="search-box">
        <input type="text" class="search" placeholder="Search...">
      </div>
    </main>
  </div>
  <router-view/>
</template>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#app {
  background-image: url(./assets/sky-surface.jpg);
  background-size: cover;
  background-position: center;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
main {
  min-height: 100vh;
}
#nav {
  font-size:20px;
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #0af189;
    }
  }
}

.search {
  margin-top: 20px;
  width: 200px;
  height: 40px;
  padding-left: 10px;
  border-radius: 20px;
  background-color: rgba(255,255,255, 0.2);
  font-size: 18px;
}

</style>
