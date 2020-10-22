<template>
  <v-app>
    <Navbar/>
      <v-main>
        <v-container class="banner">
          <router-view/>
        </v-container>
      </v-main>
  </v-app>
</template>

<script>
import Navbar from './components/Navbar'

export default {
  name: 'App',
  components:{Navbar},
  data: () => ({
    //
  }),
};
</script>
<style>
main {
    color: #bfc1c8;
    font-family: "Roboto", "Open Sans", sans-serif;
    font-size: 14px;
    font-weight: 300;
    line-height: 1.5;
    background-color: #1e202b;
}
.banner{
  background-size: cover;
  padding: 70px 0;
  min-height: 350px; 
  background-image: url('assets/banner.png');
  background-attachment: fixed;
  background-size: 100%;
}

</style>