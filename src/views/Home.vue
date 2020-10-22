<template>
    <div>
<!--           <v-form>
            <v-container>
                <v-text-field
                    v-model="first"
                    label="First Name"
                    solo
                ></v-text-field>
                  <v-btn class="find-location">Find</v-btn>
            </v-container>
        </v-form> -->

    <!--input-->
            <v-form>
            <v-container>
            <v-row>
                <v-col cols="12">
                <v-text-field
                    v-model="find"
                    outlined
                    clearable
                    type="text"
                >
                    <template v-slot:append>
                    <v-fade-transition leave-absolute>
                        <v-progress-circular
                        v-if="loading"
                        size="24"
                        color="info"
                        indeterminate
                        >
                         <v-btn class="find-location">Find</v-btn> </v-progress-circular> 
                       
                    </v-fade-transition>
                    </template>
                </v-text-field>
                </v-col>
            </v-row>
            </v-container>
        </v-form>
<!--tabla tiempo-->
                <div class="container">
            <h3>Users:</h3>
                <table class="table">
            <thead>
            <tr>
            <th scope="col">Id</th>
                    <th scope="col">Name</th>
                    </tr>
                </thead>
                <tbody>
            <tr v-for="user in users" v-bind:key="user.id"> 
            <th scope="row">{{user.id}}</th>
                    <td>{{weather.name}}</td>
                    </tr>
                </tbody>
                </table> 
            </div> 
    </div>

    
</template>

<script>
import axios from "axios";
export default {
    data(){
        return {
            weather:[],
            message: 'Hey!',
            loading: false,
        }
    },
    methods:{
        async getWeather(){
            let datos = await axios.get('../data.json')
            console.log(datos);
        },
        clickMe () {
        this.loading = true
        this.message = 'Wait for it...'
        setTimeout(() => {
          this.loading = false
          this.message = `You've clicked me!`
        }, 2000)
      }
    },
    created(){
        this.getWeather()
    }
}
</script>

<style>
.container {
  margin-right: auto;
  margin-left: auto;
  padding-left: 15px;
  padding-right: 15px;
  *zoom: 1; }
  
.find-location {
  position: relative;
  margin-bottom: 70px; }
  .find-location input[type="text"] {
    width: 100%;
    padding: 20px 50px 20px 20px;
    background: #1e202b;
    color: white; }
  .find-location input[type="submit"] {
    position: absolute;
    top: 5px;
    right: 5px;
    bottom: 5px;
    padding: 0 40px; }
    .button, form input[type="submit"], form button, form input[type="reset"] {
    border: none;
    background: #009ad8;
    padding: 10px 20px;
    border-radius: 30px;
    color: white;
}
.find-location input[type="text"] {
    width: 100%;
    padding: 20px 50px 20px 20px;
    background: #1e202b;
    color: white;
}
form input, form textarea, form select {
    outline: none;
    border: none;
    padding: 10px;
    border-radius: 30px;
}
</style>
