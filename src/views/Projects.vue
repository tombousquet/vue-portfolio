<template>
  <div class='about pa-6'>
    <h1> My projects page </h1>
    <v-container>
        <v-row>
          <v-col
          >
<v-card
    class="mx-auto pt-2 mt-4"
    max-width="344"
    v-for="project in projects"
          :key="project.id"
  >
    <v-img
      :src="project.image"
      height="200px"
    ></v-img>

    <v-card-title>
      {{project.title}}
    </v-card-title>

    <v-card-subtitle>
      {{project.sub}}
    </v-card-subtitle>

    <v-card-actions>
      <v-btn
        color="orange lighten-2"
        text
      >
        Explore
      </v-btn>

      <v-spacer></v-spacer>

      <v-btn
        icon
        @click="show = !show"
      >
        <v-icon>{{ show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
      </v-btn>
    </v-card-actions>

    <v-expand-transition>
      <div v-show="show">
        <v-divider></v-divider>

        <v-card-text>
          {{project.text}}
        </v-card-text>
      </div>
    </v-expand-transition>
  </v-card>          </v-col>
        </v-row>
      </v-container>
  </div>
</template>

<script>
  export default {
    data: () => ({
      show: false,
      projects: [
        {id: '1', image: "thisland.png", title: "This Land" , sub: "Share personal histories about you community" , text: "I'm a thing. But, like most politicians,"},
        {id: '2', image: "booktracker.png", title: "BookTracker" , sub: "What's on your reading list?" , text: "I'm a thing. But, like most politicians,"},
        {id: '3', image: "kys.png", title: "KnowYourStuff" , sub: "Test your knowledge" , text: "I'm a thing. But, like most politicians,"},
        ],
        }),
  }
</script>