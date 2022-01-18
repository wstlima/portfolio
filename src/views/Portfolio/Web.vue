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
        max-width="100%"
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
              <v-card-title primary-title class="justify-center">{{
                project.title
              }}</v-card-title>
            </v-card>
          </v-flex>
        </template>
        <v-card v-if="project.dialog">
          <v-carousel :continuous="true" height="auto">
            <v-carousel-item
              eager
              v-for="(item, i) in project.items"
              :key="i"
              :src="item.src"
            ></v-carousel-item>
          </v-carousel>

          <!-- <v-img :src="project.poster"></v-img> -->
          <v-card-text>
            <h3 class="headline mb-0">
              <span>{{ project.title }}</span>
            </h3>
            <h4 class="green--text mb-4">
              <span>{{ project.desc }}</span>
            </h4>
            <v-chip color="green" text-color="white">{{
              project.tech.tech1
            }}</v-chip>
            <v-chip color="green" text-color="white">{{
              project.tech.tech2
            }}</v-chip>
            <v-chip color="green" text-color="white">{{
              project.tech.tech3
            }}</v-chip>
            <v-chip color="green" text-color="white">{{
              project.tech.tech4
            }}</v-chip>
          </v-card-text>
          <v-card-actions>

            <v-btn  v-if="project.git!='#'"
              flat
              large
              dark
              color="green"
              :href="project.git"
              target="_blank"
            >
              <v-icon left>fab fa-github</v-icon>GitHub
            </v-btn>

            <v-btn  v-if="project.behance!='#'"
              flat
              large
              dark
              color="green"
              :href="project.behance"
              target="_blank"
            >
              <v-icon left>fab fa-behance</v-icon>Behance
            </v-btn>

            <v-btn  v-if="project.prot!='#'"
              flat
              large
              dark
              color="green"
              :href="project.prot"
              target="_blank"
            >
              <v-icon left>fas fa-object-group</v-icon>Protótipo
            </v-btn>


            
            <v-btn v-if="project.demo!='#'"
              large
              flat
              dark
              color="green"
              :href="project.demo"
              target="_blank"
            >
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
    title: "Web Portfolio",
    titleTemplate: "%s ← Dev Well Lima",
    meta: [
      { name: "viewport", content: "width=device-width, initial-scale=1" },
      {
        name: "description",
        content:
          "Dev Well Lima Web Portfolio Vue Vue.js Nuxt Nuxt.js HTML CSS Vuetify Axios GraphQL JavaScript Web Developer Front-End Frontend Designer App Responsive",
      },
      { charset: "utf-8" },
      { property: "og:title", content: "Dev Well Lima" },
      { property: "og:site_name", content: "Dev Well Lima" },
      { property: "og:type", content: "website" },
      { property: "og:url", content: "https://well.controlemix.com.br" },
      {
        property: "og:image",
        content: "/assets/images/avatar.jpg",
      },
      {
        property: "og:description",
        content:
          "Dev Well Lima Web Portfolio Vue Vue.js Nuxt Nuxt.js HTML CSS Vuetify Axios GraphQL JavaScript Web Developer Front-End Frontend Designer App Responsive",
      },
    ],
  },
  data() {
    return {
      dialog: false,
      projects: [
        {
          dialog: false,
          title: "Controle de Gastos",
          desc: "Aplicação web usando PouchDB para rodar off line e com recursos de checkout para pagamento recorrente de assinaturas.",
          git: "#",
          behance: "https://www.behance.net/gallery/117197767/UX-Controle-de-Gastos-Web",
          prot: "https://xd.adobe.com/view/671815bb-ccf5-4bbe-9c29-90ab401939ac-324b/",
          demo: "https://controlemix.com.br",
          tech: {
            tech1: "Vue",
            tech2: "PWA",
            tech3: "SCSS",
            tech4: "Node.js",
          },
          poster: "/assets/images/webapps/proj1/p1.jpg",
          items: [
            {
              src: "/assets/images/webapps/proj1/p1.jpg",
            },
            {
              src: "/assets/images/webapps/proj1/p2.jpg",
            },
            {
              src: "/assets/images/webapps/proj1/p3.jpg",
            },
            {
              src: "/assets/images/webapps/proj1/p4.jpg",
            },
            {
              src: "/assets/images/webapps/proj1/p5.jpg",
            }            
          ],
        },
        {
          dialog: false,
          title: "Este Site",
          desc: "Site integrado com Firebase, Storyblock, Google Analytics",
          git: "https://github.com/wstlima/portfolio",
          behance: "#",
          prot: "#",
          demo: "https://well.controlemix.com.br/",
          tech: {
            tech1: "VUE",
            tech2: "Storyblok",
            tech3: "HTML",
            tech4: "JavaScript",
          },
          poster: "/assets/images/webapps/proj2/p1.jpg",
          items: [
            {
              src: "/assets/images/webapps/proj2/p1.jpg",
            },
            {
              src: "/assets/images/webapps/proj2/p2.jpg",
            },
            {
              src: "/assets/images/webapps/proj2/p3.jpg",
            },
            {
              src: "/assets/images/webapps/proj2/p4.jpg",
            },
            {
              src: "/assets/images/webapps/proj2/p5.jpg",
            }            
          ],
        },
        {
          dialog: false,
          title: "Clube de Assinantes Intrínsecos",
          desc: "Aplicativo SPA para controle de assinaturas",
          git: "#",
          behance: "https://www.behance.net/gallery/112298499/Portfolio-Clube-Assinante",
          prot: "#",
          demo: "https://stag.sintrin.com.br",
          tech: {
            tech1: "Angular",
            tech2: "SCSS",
            tech3: "HTML",
            tech4: "JavaScript",
          },
          poster: "/assets/images/webapps/proj3/p1.jpg",
          items: [
            {
              src: "/assets/images/webapps/proj3/p1.jpg",
            },
            {
              src: "/assets/images/webapps/proj3/p2.jpg",
            },
            {
              src: "/assets/images/webapps/proj3/p3.jpg",
            },
            {
              src: "/assets/images/webapps/proj3/p4.jpg",
            },
            {
              src: "/assets/images/webapps/proj3/p5.jpg",
            }            
          ],
        },
      ],
    };
  },
};
</script>

<style  scoped>
</style>
