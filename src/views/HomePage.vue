<template>
    <div class="container">
        <div class="row">
            <div class="col-md head">
                <!-- <h4>Hello {{ name }} welcome to homepage</h4> -->

            </div>
        </div>

        <div class="row mt-3">
            <div class="col">
                <table class="table table-bordered" border="3" >
                    
                        <tr class="tHead">
                            <td>Id</td>
                            <td>Name</td>
                            <td>Location</td>
                            <td>Actions</td>
                            <td>Actions</td>
                        </tr>
                    
                    <tr v-for="item in restaurant" :key="item.id">
                        <td>{{ item.id }}</td>
                        <td>{{ item.name }}</td>
                        <td>{{ item.location }}</td>
                        <td> <router-link :to="'/updateRestaurant/'+item.id">Update Restaurant</router-link> </td>
                        <td><button v-on:click="deleteRestaurant(item.id)" type="button" class="btn btn-lg btn-success" ><font-awesome-icon :icon="['fas', 'trash']" /></button></td>
                        </tr>
                </table>
            </div>
        </div>
    </div>
</template>

<script>
import axios from 'axios';

    export default {
        data () {
    return {
      name:'',
      restaurant: []
    }
  },

    methods: {
      async  deleteRestaurant (id) {
            let result = await axios.delete("https://foodieapi-u2rl.onrender.com/restaurant/"+id);     
                if(result.status==200)
               {
                this.loadData()
                }
        },
        
        async loadData() {
            let user = localStorage.getItem('info');
    //   if(user) {
    //     this.name = JSON.parse(user).name;

    //   }
    //   else
    //   {
    //     this.$router.push({name:'homePage'});
    //   } 

      let result = await axios.get("https://foodieapi-u2rl.onrender.com/restaurant");
      console.warn(result)
      this.restaurant = result.data
        }
    },

   async  mounted()
   {
      
      this.loadData();  
    }
    }
</script>

<style scoped>
    table {
      border-collapse: collapse;
      width: 100%;
    }

    th, td {
      border: 1px solid #198754;
      padding: 20px;
      text-align: left;
    }

    th {
      background-color: #333;
    }
    p{
        color: rgb(236, 72, 72);
    }
    td{
      text-decoration: none;
    }
    tr{
      padding: 10px;
    }
    .tHead{
      color: #198754;
      font-weight: 600;
      
    }
    a{
      text-decoration: none;
    }
    .btn{
      background-color: #198754;
    }

    @media only screen and (max-width: 767px) {
      th, td {
        padding: 7px;
      }
      
    }
</style>