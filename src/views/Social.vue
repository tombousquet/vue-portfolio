<template>
  <div class='about pa-6'>
    <v-container class='pa-6 mt-12'>
      <v-row>
        <v-col cols=4
          v-for="social in socials"
            :key="social.id">
          <v-card
            flat
            class="mx-auto pt-2 mt-4"
            max-width="344"
            :to='social.to'
            link
          >
            <v-card-title class='display-2 teal--text teal--lighten-1'>
              {{social.title}}
            </v-card-title>
            <v-card-subtitle class='title'>
              {{social.sub}}
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
          { title: 'LinkedIn', sub: 'linkedin.com/in/tom-bousquet', to:'https://www.linkedin.com/in/tom-bousquet/' },
          { title: 'GitHub', sub: 'github.com/tombousquet', to:'https://github.com/tombousquet' },
          { title: 'Medium', sub: 'tom-bousquet.medium.com/', to:'https://tom-bousquet.medium.com/' },
        ],
        }),
  }
</script>

