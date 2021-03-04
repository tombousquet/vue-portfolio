<template>
  <div class='about pa-6'>
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