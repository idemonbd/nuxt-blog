<template>
  <div id="app">
    <Header />
    <nuxt />
  </div>
</template>

<script>
export default {};
</script>

<style lang="css">

/* GLOBAL STYLES */

body {
  font-family: system-ui;
}

a,
a:hover {
  text-decoration: none;
}

ul {
  list-style: none;
}

/* CUSTOM STYLES */
header {
  background: rgb(0, 0, 0);
}

nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 1200px;
  height: 70px;
  margin: auto;
}

nav h1.brand a {
  font-size: 24pt;
  color: rgb(255, 255, 255);
}

nav ul {
  display: flex;
  align-items: center;
}

nav ul li a {
  background: #292929;
  color: white;
  padding: 10px 20px;
  margin: 0px 10px;
}

nav ul li a:hover,
nav ul li a.nuxt-link-exact-active {
  color: white;
  border-bottom: 2px solid;
}
</style>