<template>
  <v-layout row justify-center align-center wrap class="mt-4 pt-2">
    <v-flex
      xs12
      sm12
      md5
      lg6
      xl6
      class="mt-4 pt-4"
      style="max-width: 520px !important"
    >
      <v-card flat color="transparent" max-width="1264">
        <v-card-title primary-title>
          <div>
            <h3 class="headline mb-0 center">
              <span>Meu </span>
              <span class="green--text">Momento</span>
            </h3>
            <div>
              <p>
                Atuo como desenvolvedor especialista líder de equipe para
                construção de componentes em React para uso em um CMS, além
                disso, atuo com Phyton, Node.js, Java e também as principais
                tecnologias para aplicações Web e Mobile como React, Angular ou
                Vue.js.
              </p>
            </div>
          </div>
        </v-card-title>
      </v-card>
    </v-flex>
    <v-flex
      xs12
      sm12
      md5
      lg6
      xl6
      class="mt-4 pt-4"
      style="max-width: 520px !important"
    >
      <v-card flat color="transparent" max-width="1264">
        <v-card-title primary-title>
          <div>
            <h3 class="headline mb-0 center">
              <span>Meu </span>
              <span class="green--text">Objetivo</span>
            </h3>
            <div>
              <p>
                Colaborar como desenvolvedor especialista Full-Stack 100% remoto
                em uma equipe aplicando metodologia ágil para evoluir aplicações
                utilizando Node.js ou Phyton para Back-End com banco de dados
                modernos e para Front-End que façam uso das principais
                frameworks e libs do mercado.
              </p>
            </div>
          </div>
        </v-card-title>
      </v-card>
    </v-flex>
    <v-flex xs12 sm12 md5 lg6 xl6 style="max-width: 520px !important">
      <h2 class="mb-4 pl-4 pt-2">Formação</h2>
      <v-card-text class="py-0">
        <v-timeline align-top dense>
          <v-timeline-item color="green" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">JUN 2018</div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>Java com Testes, XML e Design Patterns</strong>
                <div class="caption mb-2">Caelum RJ</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>
          <v-timeline-item color="green" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">NOV 2015</div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>Superior em Sistemas de Informação</strong>
                <div class="caption mb-2">Unigranrio RJ</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>
          <v-timeline-item color="green" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">SET 2014</div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>2º Técnico em Processamento de Dados</strong>
                <div class="caption mb-2">Castro e Silva</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>
        </v-timeline>
      </v-card-text>
    </v-flex>
    <v-flex
      xs12
      sm12
      md4
      lg6
      xl6
      class="pt-2"
      style="max-width: 520px !important"
    >
      <h2 class="mb-4 pl-4">Experiência</h2>
      <v-card-text class="py-0">
        <v-timeline align-top dense>
          <v-timeline-item color="green" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">FEV 2021</div>
                <div class="caption font-weight-bold green--text">ATUAL</div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>Desenvolvedor Thech Leader</strong>
                <div class="caption mb-2">Editora Globo S/A</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>
          <v-timeline-item color="green" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">JUL 2020</div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>Desenvolvedor Thech Leader</strong>
                <div class="caption mb-2">Vital Connect Ltda.</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>
          <v-timeline-item color="green" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">ABR 2020</div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>Desenvolvedor Especialista</strong>
                <div class="caption mb-2">Thera Solutions Ltda.</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>
        </v-timeline>
      </v-card-text>
    </v-flex>
    <v-layout row justify-center align-center wrap class="mt-4 pt-2">
      <v-flex xs12 sm12 md4 lg5 xl5 class="mx-2 pt-4">
        <h2>
          <span>FrontEnd</span>
          <span class="green--text">Skills</span>
        </h2>
        <br />
        <strong>Vue.js / React / Angular</strong>
        <v-progress-linear
          v-model="buffer3"
          :buffer-value="bufferValue"
          color="green"
          height="16"
        ></v-progress-linear>
        <strong>HTML / CSS / JavaScript</strong>
        <v-progress-linear
          v-model="buffer2"
          :buffer-value="bufferValue"
          color="green"
          height="16"
        ></v-progress-linear>

        <strong>Grid Layout / Flexbox / Bootstrap</strong>
        <v-progress-linear
          v-model="buffer3"
          :buffer-value="bufferValue"
          color="green"
          height="16"
        ></v-progress-linear>
      </v-flex>
      <v-flex xs12 sm12 md4 lg5 xl5 class="mx-2 pt-4">
        <h2>
          <span>BackEnd</span>
          <span class="green--text">Skills</span>
        </h2>
        <br />
        <strong>Node.js / Java / Python</strong>
        <v-progress-linear
          v-model="buffer2"
          :buffer-value="bufferValue"
          color="green"
          height="16"
        ></v-progress-linear>
        <strong>MongoDB / Redis / MySQL / GraphQL</strong>
        <v-progress-linear
          v-model="buffer1"
          :buffer-value="bufferValue"
          color="green"
          height="16"
        ></v-progress-linear>
        <strong>Docker / GIT / Scrum</strong>
        <v-progress-linear
          v-model="buffer3"
          :buffer-value="bufferValue"
          color="green"
          height="16"
        ></v-progress-linear>
      </v-flex>

      <v-flex xs12 sm12 md4 lg5 xl5 class="mx-2 pt-4">
        <h2>
          <span>Devops</span>
          <span class="green--text">Skills</span>
        </h2>
        <br />
        <strong>Linux / Kubernets / Cyber Security</strong>
        <v-progress-linear
          v-model="buffer4"
          :buffer-value="bufferValue"
          color="green"
          height="16"
        ></v-progress-linear>
        <strong>Continuous Integration / Continuous Delivery</strong>
        <v-progress-linear
          v-model="buffer2"
          :buffer-value="bufferValue"
          color="green"
          height="16"
        ></v-progress-linear>

        <strong>AWS Cloud Services / Google Cloud</strong>
        <v-progress-linear
          v-model="buffer6"
          :buffer-value="bufferValue"
          color="green"
          height="16"
        ></v-progress-linear>
      </v-flex>
      <v-flex xs12 sm12 md4 lg5 xl5 class="mx-2 pt-4">
        <h2>
          <span>UIDesigner</span>
          <span class="green--text">Skills</span>
        </h2>
        <br />
        <strong>Style Guide / Design System</strong>
        <v-progress-linear
          v-model="buffer2"
          :buffer-value="bufferValue"
          color="green"
          height="16"
        ></v-progress-linear>
        <strong>Adobe XD / Figma / Zeplim</strong>
        <v-progress-linear
          v-model="buffer4"
          :buffer-value="bufferValue"
          color="green"
          height="16"
        ></v-progress-linear>
        <strong>Design Tokens / Wireframe</strong>
        <v-progress-linear
          v-model="buffer5"
          :buffer-value="bufferValue"
          color="green"
          height="16"
        ></v-progress-linear>
      </v-flex>

    </v-layout>
    <v-flex xs12 sm12 md4 lg12 xl12 class="mx-2 pt-4">
      <div  style="text-align: center">
        <div class="caption">confira mais skills</div>
        <v-btn
          href="assets/pdf/curriculo-well-lima-dev-full-stack.pdf"
          target="_blank"
          color="green"
          dark
          large
        >
          Baixar Currículo
          <v-icon right dark>fas fa-file-download</v-icon>
        </v-btn>
      </div>
    </v-flex>

    <v-flex xs12 sm12 md4 lg12 xl12 class="mx-2 pt-4">
      <div  style="text-align: center">
        <v-card-actions class="hidden-sm-and-down justify-center">
          <v-btn
            v-for="icon in icons"
            :key="icon.icon"
            fab
            dark
            outline
            color="green"
            :href="icon.href"
            target="_blank"
          >
            <v-icon dark>{{icon.icon}}</v-icon>
          </v-btn>
        </v-card-actions>

        <v-card-actions class="hidden-md-and-up justify-center">
          <v-btn
            v-for="icon in icons"
            :key="icon.icon"
            small
            fab
            dark
            outline
            color="green"
            :href="icon.href"
            target="_blank"
          >
            <v-icon dark>{{icon.icon}}</v-icon>
          </v-btn>
        </v-card-actions>
      </div>
    </v-flex>
  </v-layout>
</template>

<script>
import icons from '../data/socialIcons'

export default {
  metaInfo: {
    title: 'Currículo',
    titleTemplate: '%s ← Dev Well Lima',
    meta: [
      { name: 'viewport', content: 'width=device-width, initial-scale=1' },
      {
        name: 'description',
        content:
          'Vue NUXT HTML CSS JavaScript Design Adobe XD Photoshop Coding Skills Resume Work Web Developer Front-End'
      },
      { charset: 'utf-8' },
      { property: 'og:title', content: 'Dev Well Lima' },
      { property: 'og:site_name', content: 'Dev Well Lima' },
      { property: 'og:type', content: 'website' },
      { property: 'og:url', content: 'https://well.controlemix.com.br' },
      {
        property: 'og:image',
        content: 'assets/images/avatar.jpg'
      },
      {
        property: 'og:description',
        content:
          'Vue NUXT HTML CSS JavaScript Design Adobe XD Photoshop Coding Skills Resume Work Web Developer Front-End'
      }
    ]
  },
  data () {
    return {
      value: 0,
      buffer1: 0,
      buffer2: 0,
      buffer3: 0,
      buffer4: 0,
      buffer5: 0,
      buffer6: 0,
      bufferValue: 100,
      interval: 0,
      icons: icons
    }
  },
  mounted () {
    this.startBuffer()
  },

  beforeDestroy () {
    clearInterval(this.interval)
  },

  methods: {
    startBuffer () {
      this.interval = setInterval(() => {
        this.buffer1 = 100
        this.buffer2 = 90
        this.buffer3 = 80
        this.buffer4 = 70
        this.buffer5 = 60
        this.buffer6 = 50
      }, 800)
    }
  }
}
</script>
<style >
</style>
