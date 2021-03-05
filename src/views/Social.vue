<template>
  <div class='about'>
    <v-container class='pa-6 mt-12'>
      <v-row>
        <v-col cols=4
          v-for="social in socials"
            :key="social.id">
          <v-card
            flat
            class="mx-auto pt-2 mt-4"
            max-width="344"
          >
            <v-card-title class='display-2 grey--text grey--darken-4' >
              {{social.title}}
            </v-card-title>
            <v-card-subtitle class='title pt-1'>
              <a class='teal--text teal--lighten-1' :href='social.site' >{{social.sub}}</a>
            </v-card-subtitle>
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
      socials: [
          { title: 'LinkedIn', sub: 'linkedin.com/in/tom-bousquet', site:'https://www.linkedin.com/in/tom-bousquet/' },
          { title: 'GitHub', sub: 'github.com/tombousquet', site:'https://github.com/tombousquet' },
          { title: 'Medium', sub: 'tom-bousquet.medium.com/', site:'https://tom-bousquet.medium.com/' },
        ],
        }),
  }
</script>

