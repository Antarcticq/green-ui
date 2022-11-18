<template>
  <div id="app">
    <main-header></main-header>
    <side-nav class="side-nav"></side-nav>
    <div class="main-cnt">
      <router-view />
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  components: {},
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
}
a {
  font-weight: bold;
  color: #2c3e50;
}
.router-link-exact-active {
  color: #42b983;
}

.side-nav {
  float: left;
  width: 200px;
  /* background-color: gray; */
  height: 100%;
}

.main-cnt {
  margin-left: 210px;
  background-color: rgb(255, 255, 255);
  height: 100%;
}
</style>
