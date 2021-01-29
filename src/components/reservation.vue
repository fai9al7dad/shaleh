<template>
  <div class="d-flex justify-center">
      <v-date-picker v-model="picker" elevation="3" range ></v-date-picker>
      {{picker}}
  </div>
</template>

<script>
export default {
    data(){
        return{
            picker: '',
            allowedDate: null,
        }
    },
    methods:{
        callFunction: function () {
            var currentDate = new Date().toJSON().slice(0,10).replace(/-/g,'/');
            this.allowedDate = currentDate;
        }
    },
    mounted(){
        this.callFunction();
    }

}
</script>

<style scoped>
</style>