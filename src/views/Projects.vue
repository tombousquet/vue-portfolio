<template>
  <div class='about'>
    <v-container class='pa-6 mt-12'>
      <v-row>
        <v-col cols=4
          v-for="project in projects"
            :key="project.id">
          <v-card
            class="mx-auto pt-2 mt-4"
            max-width="344"
          >
            <v-img
              :src="project.image"
              height="200px"
            >
            </v-img>
            <v-card-title>
              <a class='teal--text teal--lighten-1' :href='project.site' >{{project.title}}</a>
            </v-card-title>
            <v-card-subtitle>
              {{project.sub}}
            </v-card-subtitle>
            <v-card-actions>
              <v-btn
              color="teal lighten-1"
              text
              >
                Learn More
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
          </v-card>         
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
  export default {
    data: () => ({
      show: false,
      projects: [
        {id: '1', image: "thisland.png", title: "This Land" , sub: "Share personal histories about your community." , site:'https://this-land.netlify.app/', text: "This Land is a React web app utilizing a Django backend and multiple MapBox features so users can find points of interest close to their location as well as add their own to the map."},
        {id: '2', image: "booktracker.png", title: "BookTracker" , sub: "What's on your reading list?" , site:'https://toms-booktracker.netlify.app/', text: "Keep track of what you've read and what you want to read while taking notes on your current book."},
        {id: '3', image: "kys.png", title: "KnowYourStuff" , sub: "Test your trivia knowledge." , site:'https://know-your-stuff.netlify.app/', text: "Think you know it all? Prove it. Try answering questions from your favorite categories."},
        ],
        }),
  }
</script>