<template>
  <v-app light>
    <tool-bar/>
    <v-content>
      <nuxt />


      <footer/>
    </v-content>
  </v-app>
</template>

<script>
import ToolBar from '~/components/ToolBar.vue'
import Footer from '~/components/Footer.vue'

export default {
  components: {
    ToolBar,
    Footer
  },
  data() {
    return {
      clipped: false,
      drawer: true,
      fixed: false,
      items: [
        { icon: 'apps', title: 'Welcome', to: '/' },
        { icon: 'bubble_chart', title: 'Inspire', to: '/inspire' }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  }
}
</script>
