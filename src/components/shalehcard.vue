<template>
<div>

    <v-row class="shalehs" >
        <v-slide-group multiple  show-arrows>
            <v-slide-item v-for="shaleh in shalehs" :key="shaleh.name" class="mx-2 my-3">
                <v-card  class="d-flex justify-center flex-column card-img"  >

                    <v-card-title class="white--text" >
                        {{shaleh.name}}
                    </v-card-title>
                    <v-card-text class="white--text">
                        {{shaleh.descrpition}}
                    </v-card-text>
                    <v-card-action>
                        <v-btn text color=primary>
                            رؤية الصور
                        </v-btn>
                    </v-card-action>
                </v-card>
            </v-slide-item>
        </v-slide-group>
    </v-row>
    
</div>
</template>

<script>
import axios from 'axios';
export default {
    data(){
        return{
            shalehs:[
                {
                   name: 'shaleh1', descrpition: 'ستة غرفة 200 ريال'
                },
                {
                   name: 'shaleh2', descrpition: '3 غرفة 600 ريال'
                },
                {
                   name: 'shaleh3', descrpition: '4 غرفة 100 ريال'
                },
                {
                   name: 'shaleh4', descrpition: '8 غرف 500 ريال'
                },
            ]
        }
    },
    mounted(){
        axios.get('192.168.1.15/shaleh').then((res)=>{
            console.log(res);
        })
    }

}
</script>

<style scoped>
.shalehs{
    background: #fff;
    padding: 20px;
}
.card-img{
     background-image: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url("https://cdn.vuetifyjs.com/images/cards/house.jpg");
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    color: #fff;
}
</style>>
