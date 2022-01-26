<template>
  <v-app>
    <Topnav :sideNaV="Sidenav"/>
    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>
import Sidenav from './components/Sidenav.vue';
import Topnav from './components/Topnav.vue'
export default {
  name: 'App',
  components: { Topnav, Sidenav },

  data: () => ({
    Sidenav:null,
  }),
  props:['SidenavMain'],
  watch:{
    Sidenav:function(vvv){
        console.log(vvv,this.Sidenav);
    }
  },
  methods:{
    
  }
};
</script>
