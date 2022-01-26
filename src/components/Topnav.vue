<template>
<v-container>
    
    <v-app-bar dense app>
        <v-app-bar-nav-icon @click="changeSideNav" ></v-app-bar-nav-icon>
        <v-app-bar-title class="success--text " >
            <span>Boychild</span>
        </v-app-bar-title>
        <v-spacer></v-spacer>
        <v-app-bar-title>
            <v-btn text color="grey">
                <span class="text-lowercase">profile</span>
                <v-icon>mdi-account</v-icon>
            </v-btn>
        </v-app-bar-title>
    </v-app-bar>
    <sidenav :sidenav="Sidenav" />
</v-container>
</template>
<script>
import Sidenav from './Sidenav.vue';
export default {
    props:['v-model','sideNaV'],
    components: { Sidenav },
    
    data(){
        return{
            Sidenav:true,
        }
    },methods:{
        changeSideNav(){
            this.Sidenav = !this.Sidenav
            console.log(this.Sidenav);
        }
    },

}
</script>

<style>

</style>