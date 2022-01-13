<template>
  <v-container grid-list-xl>
    <v-layout row justify-center align-center wrap class="mt-4 pt-2">
      <v-flex v-for="portfolio in portfolios" :key="portfolio.src" xs12 sm12 md4 lg4 xl4>
        <v-card
          :to="'/portfolio/'+(portfolio.title).toLowerCase()"
          hover
          flat
          color="transparent"
          height="230"
        >
          <v-card-title></v-card-title>
          <v-img :src="portfolio.src" aspect-ratio="2.75" height="130" contain></v-img>
          <v-card-title primary-title class="justify-center">
            <v-flex text-xs-center subheading font-weight-bold>{{portfolio.desc}}</v-flex>
          </v-card-title>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  metaInfo: {
    title: 'Portfolio',
    titleTemplate: "%s ← Dev Well Lima",
    meta: [
      { name: 'viewport', content: 'width=device-width, initial-scale=1' },
      {
        name: 'description',
        content:
          "Dev Well Lima Portfolio Web Development Video Editing Graphic Design Front-End Advetising"
      },
      { charset: 'utf-8' },
      { property: 'og:title', content: "Dev Well Lima" },
      { property: 'og:site_name', content: "Dev Well Lima" },
      { property: 'og:type', content: 'website' },
      { property: 'og:url', content: 'https://well.controlemix.com.br' },
      {
        property: 'og:image',
        content: 'assets/images/avatar.jpg'
      },
      {
        property: 'og:description',
        content:
          "Dev Well Lima Portfolio Web Development Video Editing Graphic Design Front-End Advetising"
      }
    ]
  },
  data () {
    return {
      portfolios: [
        {
          src: 'https://i.imgur.com/GvTt5GG.png',
          title: 'Web',
          desc: 'Aplicações'
        },

        {
          src: 'https://i.imgur.com/wXLtLKy.png',
          title: 'Video',
          desc: 'Vídeos'
        },
        {
          src: 'https://i.imgur.com/g74mGuU.png',
          title: 'Graphic',
          desc: 'Designers'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
</style>
