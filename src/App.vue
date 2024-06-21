<template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link :to="{name: 'about'}">About</router-link>
    <router-link :to="{name: 'jobs'}">Jobs</router-link>
  </nav>
  <button @click="redirect">SSSS</button>
  <button @click="orqaga">Orqaga</button>
  <button @click="oldinga">Oldinga</button>
  <router-view/>
</template>

<script>
export default {
  methods:{
    redirect() {
      this.$router.push({name: 'home'})
    },
    orqaga() {
      this.$router.go(-1)
    },
    oldinga() {
      this.$router.go(1)
    }
  }
}
</script>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
  text-decoration: none;
  padding: 6px 8px;
}

nav a.router-link-exact-active {
  color: #42b983;
  border: 1px solid #42b983;
  border-radius: 5px;
}
</style>
