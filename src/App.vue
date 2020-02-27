<template>
  <v-app>
    <v-app-bar
      app
      color="white"
      height="70"
    >

      <v-toolbar-title class="font-weight-black headline">
        <v-img
          contain
          max-height="60"
          src="./assets/img/Picture1.png"
        ></v-img>
      </v-toolbar-title>
<v-row class="justify-space-between font-weight-black"><v-col class="col-sm-4 offset-sm-8">

        <button @click="$vuetify.goTo('#about-me')" text class="mr-4">O NAMA</button>
        <button @click="$vuetify.goTo('#smart-change')" text class="mr-4">SMART CHANGES</button>
        <button @click="$vuetify.goTo('#smart-caffe')" text class="mr-4">SMART CAFFE</button>
        <button @click="$vuetify.goTo('#usluge')" text class="mr-4">USLUGE</button>
      </v-col></v-row>
    </v-app-bar>

    <v-content>
      <section id="hero">
        <v-row no-gutters>
          <v-img
            :max-height="'calc(100vh - ' + $vuetify.application.top + 'px)'"
            src="./assets/img/hm.jpg"
          >
            <v-theme-provider dark>
              <v-container  fill-height class="mx-auto">
                <v-row
                  align="center"
                  class="white--text mx-auto"
                  justify="center"
                >
                  <v-col
                    class="white--text text-center"
                    cols="12"
                  >
                    <div
                      class="font-weight-light"
                      :class="[$vuetify.breakpoint.smAndDown ? 'display-1' : 'display-2']"
                    >

                     <div class="text-center pa-3" >
                       <v-img
                        contain
                        height= "300px"
                        src="./assets/img/Picture1.png"
                      ></v-img>
                      </div>
                    </div>

                    <br>
                    <br>
                    <br>
                    <br>

                    <span
                      :class="[$vuetify.breakpoint.smAndDown ? 'display-4': 'display-5']"

                    >
<div class="amber--text text--accent-3 display-2 mb-7 font-weight-black">www.menjacnicasmartchange.rs</div>
                    <div class="amber--text text--accent-3 mb-7 pb-3 display-1 font-weight-black">EMAIL: SMARTKAPITALBG@GMAIL.COM KONTAKT:066/8880008</div>
                    </span>

                  </v-col>

                  <v-btn
                    class="align-self-end"
                    fab
                    outlined
                    @click="$vuetify.goTo('#about-me')"
                  >
                    <v-icon>mdi-chevron-double-down</v-icon>
                  </v-btn>
                </v-row>
              </v-container>
            </v-theme-provider>
          </v-img>
        </v-row>
      </section>
       <Onama></Onama>
      <SmartChanges></SmartChanges>
      <SmartCafe></SmartCafe>
      <Lokacije></Lokacije>
      <Usluge></Usluge>
      <Intro></Intro>

      <About></About>

      <v-sheet
        id="contact"
        color="#333333"
        dark
        tag="section"
        tile
      >
        <div class="py-12"></div>

        <!-- <v-container>
          <h2 class="display-2 font-weight-bold mb-3 text-uppercase text-center">Contact Me</h2>

          <v-responsive
            class="mx-auto mb-12"
            width="56"
          >
            <v-divider class="mb-1"></v-divider>

            <v-divider></v-divider>
          </v-responsive>

          <v-theme-provider light>
          </v-theme-provider>
        </v-container> -->

        <div class="py-12"></div>
      </v-sheet>
    </v-content>

    <v-footer
      class="justify-center"
      color="#292929"
      height="100"
    >
      <div class="title font-weight-light grey--text text--lighten-1 text-center">
        &copy; {{ (new Date()).getFullYear() }} — kollence.github.io — Made with 💜 by misterija@gmail.com
      </div>
    </v-footer>
  </v-app>

</template>

<script>
// @ is an alias to /src
import SmartChanges from './views/SmartChanges'
import Onama from './views/Onama'
import Lokacije from './views/Lokacije'
import Usluge from './views/Usluge'
import SmartCafe from './views/SmartCafe'
import Intro from './views/Intro'
import About from './views/About'
export default {
  components: {
    SmartChanges,
    Onama,
    Lokacije,
    Usluge,
    SmartCafe,
    Intro,
    About
  },
  data () {
    return {
      windowSize: true,
      articles: [
        {
          src: 'https://images.unsplash.com/photo-1423784346385-c1d4dac9893a?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1950&q=80',
          title: 'Mobile first & Responsive',
          text: 'Phasellus lorem enim, luctus ut velit eget, convallis egestas eros. Sed ornare ligula eget tortor tempor, quis porta tellus dictum.'
        },
        {
          src: 'https://images.unsplash.com/photo-1475938476802-32a7e851dad1?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1950&q=80',
          title: 'Think outside the box',
          text: 'Nam ut leo ipsum. Maecenas pretium aliquam feugiat. Aenean vel tempor est, vitae tincidunt risus. Sed sodales vestibulum nibh.'
        },
        {
          src: 'https://images.unsplash.com/photo-1416339442236-8ceb164046f8?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1892&q=80',
          title: 'Small changes, big difference',
          text: 'Vestibulum in dictum velit, in rhoncus nibh. Maecenas neque libero, interdum a dignissim in, aliquet vitae lectus. Phasellus lorem enim, luctus ut velit eget.'
        }
      ],
      features: [
        {
          icon: 'mdi-account-group-outline',
          title: 'Vibrant Community',
          text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Iusto cupiditate sint possimus quidem atque harum excepturi nemo velit tempora! Enim inventore fuga, qui ipsum eveniet facilis obcaecati corrupti asperiores nam'
        },
        {
          icon: 'mdi-update',
          title: 'Frequent Updates',
          text: 'Sed ut elementum justo. Suspendisse non justo enim. Vestibulum cursus mauris dui, a luctus ex blandit. Lorem ipsum dolor sit amet consectetur adipisicing elit. qui ipsum eveniet facilis obcaecati corrupti consectetur adipisicing elit.'
        },
        {
          icon: 'mdi-shield-outline',
          title: 'Long-term Support',
          text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Iusto cupiditate sint possimus quidem atque harum excepturi nemo velit tempora! Enim inventore fuga, qui ipsum eveniet facilis obcaecati corrupti asperiores nam'
        }
      ],
      drawer: true,
      items: [
        { title: 'Dashboard', icon: 'mdi-view-dashboard' },
        { title: 'Photos', icon: 'mdi-image' },
        { title: 'About', icon: 'mdi-help-box' }
      ],
      color: 'primary',
      colors: [
        'primary',
        'blue',
        'success',
        'red',
        'teal'
      ],
      right: true,
      miniVariant: false,
      expandOnHover: false,
      background: false

    }
  },
  computed: {
    bg () {
      return this.background ? 'https://cdn.vuetifyjs.com/images/backgrounds/bg-2.jpg' : undefined
    }
  }
}
</script>
