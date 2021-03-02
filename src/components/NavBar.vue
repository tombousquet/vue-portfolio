<template>
  <nav>
    <v-app-bar>
    <v-app-bar-nav-icon class="grey--text" >email</v-app-bar-nav-icon>
    </v-app-bar>



      

      <v-navigation-drawer app v-model="drawer" class="indigo">
        <v-list>
          <v-list-tile>
            <v-list-tile-action>
            </v-list-tile-action>
          </v-list-tile>
        </v-list>
      </v-navigation-drawer>
    

  </nav>
</template>

<script>
  export default {
    data() {
      return {
        drawer: false
      }
    }
  }
    
</script>
