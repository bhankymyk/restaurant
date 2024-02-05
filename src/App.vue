<template>
  <div class="container">
    <div class="row">
      <div class="col">
        <nav>
          <router-link to="/">FOOD-IE </router-link> 
          <router-link to="/homePage"> <font-awesome-icon :icon="['fas', 'house']" /> Home </router-link> 
          <router-link to="/addRestaurant"> <font-awesome-icon :icon="['fas', 'square-plus']" /> Add Restaurant </router-link> 
          <router-link to="/about"> <font-awesome-icon :icon="['fas', 'address-card']" /> About </router-link> 
        </nav>
        <router-view/>
      </div>
    </div>
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  /* color: #2c3e50; */
}

nav {
  padding: 20px;
  justify-content: space-around;
  display: flex;
}

nav a {
  color: #42b983;
  font-weight: bold;
  /* color: #2c3e50; */
  text-decoration: none;
}
nav a.router-link-exact-active {
  color: #42b983;
}

@media  only screen and (max-width: 767px) {
  nav{
    padding: 5px;
    /* display: block; */
    /* margin-right: 5px; */
  }
  
}
</style>
