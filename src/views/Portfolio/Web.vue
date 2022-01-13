<template>
  <v-container grid-list-xl>
    <h2 class="pl-4">
      <span>Web</span>
      <span class="green--text">Apps</span>
    </h2>
    <v-layout row justify-center align-center wrap class="mt-4 pt-2">
      <v-dialog
        v-model="project.dialog"
        lazy
        max-width="1000"
        v-for="project in projects"
        :key="project.title"
      >
        <template v-slot:activator="{ on }">
          <v-flex xs12 sm6 md4 lg4 xl4 v-on="on">
            <v-card hover flat color="transparent">
              <v-img
                :src="project.poster"
                :alt="project.title"
                height="230"
                lazy-src="https://cdn.dribbble.com/users/503653/screenshots/3143656/fluid-loader.gif"
              ></v-img>
              <v-card-title primary-title class="justify-center">{{project.title}}</v-card-title>
            </v-card>
          </v-flex>
        </template>
        <v-card v-if="project.dialog">
          <v-img :src="project.poster"></v-img>
          <v-card-text>
            <h3 class="headline mb-0">
              <span>{{project.title}}</span>
            </h3>
            <h4 class="green--text mb-4">
              <span>{{project.desc}}</span>
            </h4>            
            <v-chip color="green" text-color="white">{{project.tech.tech1}}</v-chip>
            <v-chip color="green" text-color="white">{{project.tech.tech2}}</v-chip>
            <v-chip color="green" text-color="white">{{project.tech.tech3}}</v-chip>
            <v-chip color="green" text-color="white">{{project.tech.tech4}}</v-chip>
          </v-card-text>
          <v-card-actions>
            <v-btn flat large dark color="green" :href="project.git" target="_blank">
              <v-icon left>fab fa-github</v-icon>GitHub
            </v-btn>
            <v-btn large flat dark color="green" :href="project.demo" target="_blank">
              <v-icon left>fas fa-desktop</v-icon>Demo
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-dialog>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  metaInfo: {
    title: 'Web Portfolio',
    titleTemplate: "%s ← Dev Well Lima",
    meta: [
      { name: 'viewport', content: 'width=device-width, initial-scale=1' },
      {
        name: 'description',
        content:
          "Dev Well Lima Web Portfolio Vue Vue.js Nuxt Nuxt.js HTML CSS Vuetify Axios GraphQL JavaScript Web Developer Front-End Frontend Designer App Responsive"
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
          "Dev Well Lima Web Portfolio Vue Vue.js Nuxt Nuxt.js HTML CSS Vuetify Axios GraphQL JavaScript Web Developer Front-End Frontend Designer App Responsive"
      }
    ]
  },
  data () {
    return {
      dialog: false,
      projects: [
        {
          dialog: false,
          title: 'Controle de Gastos',
          desc: 'Aplicação web usando PouchDB para rodar off line',
          git: '#',
          demo: 'https://controlemix.com.br',
          tech: {
            tech1: 'Vue',
            tech2: 'JavaScript',
            tech3: 'SCSS',
            tech4: 'Markdown'
          },
          poster: 'https://well.controlemix.com.br/assets/images/controlemix1.jpg'
        },
        {
          dialog: false,
          title: 'Este Site',
          desc: 'Site integrado com Firebase, Storyblock, Google Analytics',
          git: '#',
          demo: 'https://well.controlemix.com.br/',
          tech: {
            tech1: 'VUE',
            tech2: 'Storyblok',
            tech3: 'HTML',
            tech4: 'JavaScript'
          },
          poster: 'https://well.controlemix.com.br/assets/images/site1.jpg'
        },
        {
          dialog: false,
          title: 'Clube de Assinantes Intrínsecos',
          desc: 'Aplicativo SPA para controle de assinaturas',
          git: '#',
          demo: 'https://www.intrinsecos.com.br',
          tech: {
            tech1: 'Angular',
            tech2: 'SCSS',
            tech3: 'HTML',
            tech4: 'JavaScript'
          },
          poster: 'https://well.controlemix.com.br/assets/images/intri1.jpg'
        }
      ]
    }
  }
}
</script>

<style  scoped>
</style>
