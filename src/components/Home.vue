<template>
    <div class="small-screen">
    <div class="row  mb-5 text-center">
      <img src="" alt="">
      <!-- <img src="../assets/Illustartion.png" class="img-fluid" alt=""> -->
      <div class="col">

      </div>
    </div>

    <div class="row">
      <div class="col-md-6">
        <!-- <h2>Hello {{ name}}, welcome to homepage</h2> -->
      </div>
    </div>
    <div class="row">
      <div class="col-md-12 text-center">
        <h3>Find Restaurant Management<br> made easy as pie</h3>
        <p> Very easy to add, update and <br> delete a restaurant. Enjoy!!!</p>
        <button class="btn btn-lg btn-success" type="button">
          <router-link to="/homePage">Next</router-link></button>
      </div>
    </div>
  </div>

</template>

<script>
export default {
  name: 'Home',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
a {
  color: #42b983;
}
button{
  /* background-color: #42b983; */
  padding: 10px 20px;
  font-size: 20px;
  width: 200px;
  
}

a {
  text-decoration: none;
  color: white;
  font-weight: 600;
}
.small-screen{
  background: url("../assets/Pattern.png");
    height: 100vh;

}

/* 
@media only screen and (max-width: 767px) {
  .small-screen {
    background: url("../assets/Pattern.png");
    height: 100vh;
  }
} */

</style>
