<template>
  <v-container grid-list-xl>
    <h2 class="pl-4">
      <span>UI</span>
      <span class="green--text">Portfolio</span>
    </h2>
    <v-layout row justify-center align-center wrap class="mt-4 pt-2">
      <v-dialog
        v-model="image.dialog"
        lazy
        max-width="800"
        v-for="image in images"
        :key="image.title"
      >
        <template v-slot:activator="{ on }">
          <v-flex xs12 sm6 md4 lg4 xl4 v-on="on">
            <v-card hover flat color="transparent">
              <v-img
                :src="image.poster"
                height="230"
                :alt="image.title"
                lazy-src="https://cdn.dribbble.com/users/503653/screenshots/3143656/fluid-loader.gif"
              ></v-img>
              <v-card-title primary-title class="justify-center">{{image.title}}</v-card-title>
            </v-card>
          </v-flex>
        </template>
        <v-card v-if="image.dialog">
          <v-img :src="image.poster"></v-img>
        </v-card>
      </v-dialog>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  metaInfo: {
    title: 'Graphic Portfolio ',
    titleTemplate: "%s ← Dev Well Lima",
    meta: [
      { name: 'viewport', content: 'width=device-width, initial-scale=1' },
      {
        name: 'description',
        content:
          "Dev Well Lima Graphic Adobe PhotoShop Logo Design Instagram Poster"
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
          "Dev Well Lima Graphic Adobe PhotoShop Logo Design Instagram Poster"
      }
    ]
  },
  data () {
    return {
      dialog: false,
      images: [
        {
          dialog: false,
          title: 'UI Kit App para Chatbot',
          poster: 'https://well.controlemix.com.br/assets/images/ui1.jpg'
        },
        {
          dialog: false,
          title: 'UI Kit para App de Licitações',
          poster: 'https://well.controlemix.com.br/assets/images/ui2.png'
        },
        {
          dialog: false,
          title: 'UI Kit para App para Gastos',
          poster: 'https://well.controlemix.com.br/assets/images/ui3.jpg'
        }
      ]
    }
  }
}
</script>

<style  scoped>
</style>
