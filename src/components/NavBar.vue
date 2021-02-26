<template>
  <v-card class="overflow-hidden">
    <v-app-bar
      absolute
      color="#6A76AB"
      dark
      shrink-on-scroll
      prominent
      src="https://www.goodcore.co.uk/blog/wp-content/uploads/2019/08/coding-vs-programming-2.jpg"
      fade-img-on-scroll
      scroll-target="#scrolling-techniques-3"
    >
      <template v-slot:img="{ props }">
        <v-img
          v-bind="props"
          gradient="to top right, rgba(100,115,201,.7), rgba(25,32,72,.7)"
        ></v-img>
      </template>

      <v-app-bar-title>
        <span class='subtitle-1'>Tom Bousquet</span>
        </v-app-bar-title>

      <template v-slot:extension>
        <v-tabs center-active>
          <v-tab>
            <router-link to='/social'>Social</router-link>
            </v-tab>
          <v-tab>
            Projects
            </v-tab>
          <v-tab>
            Skills
            </v-tab>
        </v-tabs>
        <v-spacer></v-spacer>
        <v-btn>
          <span>email</span>
          <v-icon>contact_mail</v-icon>
        </v-btn>
      </template>
    </v-app-bar>
    <v-sheet
      id="scrolling-techniques-3"
      class="overflow-y-auto"
      max-height="700"
    >
      <v-container style="height: 1500px;">
        <div style='height: 300px;'></div>
      </v-container>
      
    </v-sheet>
  </v-card>
  
</template>

<script>
  export default {
    name: 'NavBar',
  }
    
</script>
