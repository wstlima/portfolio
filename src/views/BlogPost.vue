<template>
  <v-layout column justify-center class="mt-4 pt-2" v-editable="result.blok">
    <h1 class="text-xs-center pb-1">{{result.title}}</h1>
    <span class="mb-4" style="text-align: center;">{{result.date.getDate()}}.{{result.date.getMonth()+1}}.{{result.date.getFullYear()}}</span>
    <v-img :src="result.image" aspect-ratio="2.75" height="330" contain :alt="result.title"></v-img>
    <v-layout column justify-center align-center class="mt-4 pt-2">
      <p v-html="body"></p>
    </v-layout>
    <br>
    <br>
    <v-btn large flat to="/blog" class="green--text">
      <v-icon>arrow_back</v-icon>Voltar ao Blog
    </v-btn>
  </v-layout>
</template>

<script>
import marked from 'marked'
import StoryblokClient from 'storyblok-js-client'
// const token = 'dbkdP7YPwIowdqQMhwOEngtt'
const token = 'XnwBPtdnoXKNShIQQDQ43gtt'
let storyapi = new StoryblokClient({
  accessToken: token
})

export default {
  data () {
    return {
      posts: [],
      result: {}
    }
  },
  metaInfo () {
    return {
      title: this.result.title,
      titleTemplate: "%s ← Eldin's Blog",
      meta: [
        { name: 'viewport', content: 'width=device-width, initial-scale=1' },
        {
          name: 'description',
          content: this.result.content
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
          content: this.result.content
        }
      ]
    }
  },
  computed: {
    body () {
      return this.result.blok.content
    }
  },

  created () {
    window.storyblok.init({
      accessToken: token
    })
    window.storyblok.on('change', () => {
      this.getStory('home', 'draft')
    })
    window.storyblok.pingEditor(() => {
      if (window.storyblok.isInEditor()) {
        this.getStory('home', 'draft')
      } else {
        this.getStory('home', 'published')
      }
    })
  },

  methods: {
    getStory (version) {
      storyapi
        .get('cdn/stories', {
          version: 'draft',
          starts_with: 'blog/'
        })
        .then(res => {
          this.posts = res.data.stories.map(bp => {
            console.log(bp);
            return {
              id: bp.slug,
              title: bp.content.title,
              blok: bp.content,
              image: bp.content.thumbnail,
              content: bp.content.content,
              date: new Date(bp.content.date)
              // date: new Date(bp.content.date)
            }
          })
          this.result = this.posts.find(
            rightPost => rightPost.id === this.$route.params.id
          )
        })
        .catch(error => {
          console.log(error)
        })
    }
  }
}
</script>

<style scoped>
.language-javascript {
    width: -webkit-fill-available !important;
}

.code {
    background-color: #272822;
}
</style>
