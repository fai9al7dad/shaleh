<template>
  <v-app>
    <v-main>
        <v-app-bar class="d-flex justify-center" color="white" dense>
          <v-app-bar-title>{{shaleh.name}}</v-app-bar-title>
        </v-app-bar>
        <router-view></router-view>
    </v-main> 
  </v-app>
</template>

<script>
import Home from '@/views/Home';
export default {
  name: 'App',
  components:{
    'home-page': Home
  },
  data(){
    return{
      shaleh:{
        name: 'شاليه الافراح'
      }
    }
  }
}

</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Tajawal:wght@400;700&display=swap');

*{
  font-family: 'Tajawal', sans-serif;
}
#app{
  background:#fbfbfb;
}
</style>
