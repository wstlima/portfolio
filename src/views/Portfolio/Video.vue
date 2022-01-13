<template>
  <v-container grid-list-xl>
    <h2 class="pl-4">
      <span>Video</span>
      <span class="green--text">Portfolio</span>
    </h2>
    <v-layout row justify-center align-center wrap class="mt-4 pt-2">
      <v-dialog
        v-model="video.dialog"
        lazy
        max-width="800"
        v-for="video in videos"
        :key="video.title"
      >
        <template v-slot:activator="{ on }">
          <v-flex xs12 sm6 md4 lg4 xl4 v-on="on">
            <v-card hover flat color="transparent">
              <v-img
                :src="video.poster"
                aspect-ratio="1.7778"
                :alt="video.title"
                lazy-src="https://cdn.dribbble.com/users/503653/screenshots/3143656/fluid-loader.gif"
                contain
              ></v-img>
              <v-card-title primary-title class="justify-center">{{video.title}}</v-card-title>
            </v-card>
          </v-flex>
        </template>
        <v-card v-if="video.dialog">
          <plyr>
            <div class="plyr__video-embed">
              <iframe :src="video.href" allowfullscreen allowtransparency allow="autoplay"></iframe>
            </div>
          </plyr>
        </v-card>
      </v-dialog>
    </v-layout>
  </v-container>
</template>

<script>
import { PlyrVideo } from 'vue-plyr'

export default {
  metaInfo: {
    title: 'Video Portfolio',
    titleTemplate: "%s ← Dev Well Lima",
    meta: [
      { name: 'viewport', content: 'width=device-width, initial-scale=1' },
      {
        name: 'description',
        content:
          "Dev Well Lima Services Adobe Premire After Effects Video Ad's Social Media Logo Animation Instagram Facebook Video Editing Advetising"
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
          "Dev Well Lima Services Adobe Premire After Effects Video Ad's Social Media Logo Animation Instagram Facebook Video Editing Advetising"
      }
    ]
  },
  components: { plyr: PlyrVideo },
  data () {
    return {
      dialog: false,
      videos: [
        {
          dialog: false,
          title: 'Aula #1 - PagSeguro Checkout Transparente Ionic',
          href: 'https://www.youtube.com/embed/1xWgE0pqypg',
          type: 'text/html',
          youtube: '1xWgE0pqypg',
          poster: 'https://img.youtube.com/vi/1xWgE0pqypg/maxresdefault.jpg'
        },
        {
          dialog: false,
          title: 'Aula #2 - PagSeguro Checkout Transparente Ionic',
          href: 'https://www.youtube.com/embed/wGODP_lY2R0',
          type: 'text/html',
          youtube: 'wGODP_lY2R0',
          poster: 'https://img.youtube.com/vi/wGODP_lY2R0/maxresdefault.jpg'
        },
        {
          dialog: false,
          title: 'Aula #3 - PagSeguro Checkout Transparente Ionic',
          href: 'https://www.youtube.com/embed/m-VDZjIZ7eY',
          type: 'text/html',
          youtube: 'm-VDZjIZ7eY',
          poster: 'https://img.youtube.com/vi/m-VDZjIZ7eY/maxresdefault.jpg'
        },
        {
          dialog: false,
          title: 'Aula #4 - PagSeguro Checkout Transparente Ionic',
          href: 'https://www.youtube.com/embed/jnJvZM3-B9k',
          type: 'text/html',
          youtube: 'jnJvZM3-B9k',
          poster: 'https://img.youtube.com/vi/jnJvZM3-B9k/maxresdefault.jpg'
        },
        {
          dialog: false,
          title: 'Aula #5 - PagSeguro Checkout Transparente Ionic',
          href: 'https://www.youtube.com/embed/DGFt_miMX1c',
          type: 'text/html',
          youtube: 'DGFt_miMX1c',
          poster: 'https://img.youtube.com/vi/DGFt_miMX1c/maxresdefault.jpg'
        },
        {
          dialog: false,
          title: 'Instale o Vesta CP + CSF Firewall',
          href: 'https://www.youtube.com/embed/YcKIz7vrvbI',
          type: 'text/html',
          youtube: 'YcKIz7vrvbI',
          poster: 'https://img.youtube.com/vi/YcKIz7vrvbI/maxresdefault.jpg'
        },
        {
          dialog: false,
          title: 'Restauração do Backup do Sistema',
          href: 'https://www.youtube.com/embed/L_J1q0O-N9c',
          type: 'text/html',
          youtube: 'L_J1q0O-N9c',
          poster: 'https://img.youtube.com/vi/L_J1q0O-N9c/maxresdefault.jpg'
        },
        {
          dialog: false,
          title: 'Plugin Especial Yoast SEO',
          href: 'https://www.youtube.com/embed/jzKPKZkPm-s',
          type: 'text/html',
          youtube: 'jzKPKZkPm-s',
          poster: 'https://img.youtube.com/vi/jzKPKZkPm-s/maxresdefault.jpg'
        },
        {
          dialog: false,
          title: 'Plugin Especial Visual Composer',
          href: 'https://www.youtube.com/embed/kiHuWUeWE-c',
          type: 'text/html',
          youtube: 'kiHuWUeWE-c',
          poster: 'https://img.youtube.com/vi/kiHuWUeWE-c/maxresdefault.jpg'
        }        
      ]
    }
  }
}
</script>

<style  scoped>
@import "../../../node_modules/vue-plyr/dist/vue-plyr.css";
</style>
