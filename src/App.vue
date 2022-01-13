<template>
  <v-app :dark="goDark">
    <v-content>
      <v-container align-center>
        <TheHeader :goDark="goDark" @changeTheme="updateTheme($event)"/>

        <transition
          name="router-animation"
          mode="out-in"
          enter-active-class="animated fadeIn fast"
          leave-active-class="animated fadeOut faster"
        >
          <router-view></router-view>
        </transition>
      </v-container>
    </v-content>
    <TheFooter/>
  </v-app>
</template>

<script>
import TheHeader from './components/TheHeader'
import TheFooter from './components/TheFooter'

export default {
  name: 'App',
  metaInfo: {
    title: 'Home',
    titleTemplate: "%s ← Dev Well Lima",
    meta: [
      { name: 'viewport', content: 'width=device-width, initial-scale=1' },
      { name: 'description', content: "Dev Well Lima Portfolio" },
      { charset: 'utf-8' },
      { property: 'og:title', content: "Dev Well Lima" },
      { property: 'og:site_name', content: "Dev Well Lima" },
      { property: 'og:type', content: 'website' },
      { property: 'og:url', content: 'https://well.controlemix.com.br' },
      {
        property: 'og:image',
        content: 'assets/images/avatar.jpg'
      },
      { property: 'og:description', content: "Dev Well Lima Portfolio" }
    ]
  },
  components: {
    TheHeader,
    TheFooter
  },
  data () {
    return { goDark: false }
  },
  methods: {
    updateTheme (updatedTheme) {
      this.goDark = !updatedTheme
    }
  }
}
</script>
<style>
@import "/assets/css/animate.min.css";
</style>
