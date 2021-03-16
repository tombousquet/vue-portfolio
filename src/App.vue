<template>
  <v-app id="inspire">
    <v-navigation-drawer v-model='drawer' app>
      <v-list-item>
        <v-list-item-content>
          <v-list-item-title class="title teal--text text--lighten-1">
            Tom Bousquet
          </v-list-item-title>
          <v-list-item-subtitle>
            Software Developer
          </v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list
        dense
        nav
      >
        <v-list-item
          v-for="item in items"
          :key="item.title"
          :to='item.to'
          link
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title class='teal--text text--lighten-1'>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar
      app
      color="#primary"
      dark
      prominent
      src="yosemite.jpg"
      height='150'
    >
      <template v-slot:img="{ props }">
        <v-img
          v-bind="props"
          gradient="to top right, rgba(19,84,122,.5), rgba(128,208,199,.8)"
        ></v-img>
      </template>

      <v-app-bar-nav-icon @click='drawer = !drawer'></v-app-bar-nav-icon>


    </v-app-bar>

    <v-main>
      <router-view></router-view>
    </v-main>
  </v-app>
</template>

<script>
  export default {
    data: () => ({
      drawer: false,
      items: [
          { title: 'About', icon: 'emoji_people', to: '/' },
          { title: 'Projects', icon: 'mdi-view-dashboard', to: '/projects' },
          { title: 'Skills', icon: 'plus_one', to: '/skills' },
          { title: 'Social', icon: 'contact_page', to: '/social' },
          { title: 'Contact', icon: 'mail', to: '/contact' },
        ],
        }),
  }
</script>
