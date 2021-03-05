<template>
    <v-container class='pa-12 mt-6 ml-6'>
      <v-row class='pa-6'>
        <v-col
        cols='3'
         v-for="skill in skills"
          :key="skill.text">
    <v-list>
      <v-list-item-group
        color="primary"
      >
        <v-list-item
        >
          <v-list-item-icon>
            <v-icon class='black--text' v-text="skill.icon"></v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title class='title teal--text teal--lighten-1' v-text="skill.text"></v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list-item-group>
    </v-list>
        </v-col>
      </v-row>
    </v-container>
</template>

<script>
  export default {
    data: () => ({
      skills: [
          { text: 'HTML', icon: 'article' },
          { text: 'CSS', icon: 'change_history' },
          { text: 'JavaScript', icon: 'picture_in_picture' },
          { text: 'Python', icon: 'pets'},
          { text: 'Django', icon: 'polymer'},
          { text: 'React', icon: 'waves' },
          { text: 'Vue', icon: 'pageview' },
          { text: 'Tachyons', icon: 'support' },
          { text: 'Vuetify', icon: 'text_rotation_angleup' },
          { text: 'GitHub', icon: 'spa' },
          { text: 'Netlify', icon: 'offline_bolt'},
          { text: 'Agile', icon: 'view_comfy' },
          { text: 'Trello', icon: 'tune'},
        ],
        }),
  }
</script>