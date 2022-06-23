<template>
  <nav>
    <Header></Header>
  </nav>
  <router-view/>
</template>

<style>

nav {
  padding: 0px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>

<script>
import Header from "@/components/Header"

export default{
  name: "Layout",
  components: {
    Header
  }
}
</script>
