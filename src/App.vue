<template>
  <div id="app">
   
      <nav class="navbar navbar-expand navbar-dark bg-dark">
        <div class="nav navbar-nav">
      <router-link to="/" class="nav-item nav-link active">Home</router-link> |
      <router-link to="/about" class="nav-item nav-link active">About</router-link> |
      <router-link to="/user" class="nav-item nav-link active">User</router-link> |
        <router-link to="/product" class="nav-item nav-link active">Product</router-link>
    </div>
    </nav>
    <router-view/>
  </div>
</template>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
