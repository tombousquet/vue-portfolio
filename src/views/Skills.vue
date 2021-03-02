<template>
  <div class='about pa-6'>
    <h1> My skills page </h1>
    <v-list flat>
      <v-list-item-group
        color="primary"
      >
        <v-list-item
          v-for="skill in skills"
          :key="skill.text"
        >
          <v-list-item-icon>
            <v-icon v-text="skill.icon"></v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title v-text="skill.text"></v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list-item-group>
    </v-list>
  </div>
</template>

<script>
  export default {
    data: () => ({
      skills: [
          { text: 'HTML', icon: 'mdi-view-dashboard' },
          { text: 'CSS', icon: 'plus_one' },
          { text: 'JavaScript', icon: 'contact_page' },
          { text: 'Python', icon: 'mail'},
          { text: 'Django', icon: 'hail'},
          { text: 'React', icon: 'mdi-view-dashboard' },
          { text: 'Vue', icon: 'plus_one' },
          { text: 'Tachyons', icon: 'contact_page' },
          { text: 'Vuetify', icon: 'plus_one' },
          { text: 'GitHub', icon: 'contact_page' },
          { text: 'Netlify', icon: 'mail'},
          { text: 'Agile', icon: 'mdi-view-dashboard' },
          { text: 'Trello', icon: 'hail'},
        ],
        }),
  }
</script>