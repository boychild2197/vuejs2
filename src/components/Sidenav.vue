<template>
  <nav>
      <v-navigation-drawer v-model="sidenav"  color="primary" app :mini-variant.sync="mini" permanent>
          <v-list dense>
              <v-list-item>
                  <v-list-item-avatar>
                      <v-img src="https://randomuser.me/api/portraits/men/78.jpg"></v-img>
                  </v-list-item-avatar>
                  <v-list-item-title>
                      <span class="white--text display-0">John Doe</span>
                  </v-list-item-title>
              </v-list-item>
              <v-divider></v-divider>
              <v-list-item v-for="link in links" :key="link.text">
                  <v-list-item-icon>
                      <v-icon class="white--text">mdi-view-dashboard</v-icon>
                  </v-list-item-icon>
                  <v-list-item-content>
                      <v-list-item-title class="white--text">Dashboard</v-list-item-title>
                  </v-list-item-content>
              </v-list-item>
          </v-list>
      </v-navigation-drawer>
  </nav>
</template>

<script>
export default {
data(){
    return{
        drawer:true,
        mini:true,
        
        links:[
            {name:'mdi-view-dashboard', text:'Dashboard'},
            {name:'mdi-view-dashboard', text:'Dashboard'},
            {name:'mdi-view-dashboard', text:'Dashboard'},
            {name:'mdi-view-dashboard', text:'Dashboard'},
        ]
    }
},
props:['sidenav'],
watch:{

}
}
</script>

<style>

</style>