<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col">
        <nav class="navbar navbar-expand-lg">
  <div class="container-fluid">
    <a class="navbar-brand" href="#"><router-link to="/"> <img src="./assets/logo.png"  class="img-fluid" alt=""></router-link></a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
      <div class="navbar-nav">
        <a class="nav-link active" aria-current="page" href="#"><router-link to="/homePage"> <font-awesome-icon :icon="['fas', 'house']" /> Home </router-link></a>
        <a class="nav-link" href="#"> <router-link to="/addRestaurant"> <font-awesome-icon :icon="['fas', 'square-plus']" /> Add Restaurant </router-link></a>
        <a class="nav-link" href="#"><router-link to="/about"> <font-awesome-icon :icon="['fas', 'address-card']" /> About </router-link></a>
        <!-- <a class="nav-link disabled" aria-disabled="true">Disabled</a> -->
      </div>
    </div>
  </div>
</nav>


        <nav> 
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

/* nav {
  padding: 20px;
  justify-content: space-around;
  display: flex;
} */

nav a {
  color: #333;
  font-weight: bold;
  /* color: #2c3e50; */
  text-decoration: none;
}
nav a.router-link-exact-active {
  color: #42b983;
}

@media  only screen and (max-width: 767px) {
  nav{
    padding: 10px;
    display: flex;
    justify-content: space-between;
  }
  
}
</style>
