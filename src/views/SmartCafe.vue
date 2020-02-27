<template>
           <section id="smart-caffe">
        <div class="py-12"></div>

        <v-container class="text-center">
          <v-row>
            <v-col justify="center" v-show="windowSize" class="justify-space-around col-md-4">
            <v-img class="mx-auto" width="300" src="../assets/img/sc.png"></v-img>
            </v-col>
            <v-col justify="center" class="text-center col-md-4 my-auto col-xs-12">
              <h2 class="display-2 font-weight-bold mb-3">SMART CAFFE</h2>
            </v-col>
            <v-col justify="center" v-show="windowSize" class="col-md-4">
            </v-col>
          </v-row>

          <v-responsive
            class="mx-auto mb-8"
            width="56"
          >
            <v-divider class="mb-1"></v-divider>

            <v-divider></v-divider>
          </v-responsive>

          <v-responsive
            class="mx-auto title font-weight-strong py-8 my-8"
            max-width="720"
          >
            “SMART KAPITAL” razvija svoje potencijale i u ugostiteljstvu.
Naše objekte možete pronaći na sledećim lokacijama:
   <div><b><i>Neznanog Junaka 4 i Vinogradska 124a</i></b></div>
          </v-responsive>
            <v-responsive>
                <v-row>
            <v-col
              v-for="({ src, text, title }, i) in articles"
              :key="i"
              cols="12"
              md="4"
            >
              <v-img
                :src="src"
                class="mb-4"
                height="275"
                max-width="100%"
              ></v-img>
            </v-col>
          </v-row>
            </v-responsive>
          <v-responsive
            class="mx-auto mb-8"
            width="56"
          >
            <v-divider class="mb-1"></v-divider>

            <v-divider></v-divider>
          </v-responsive>
        </v-container>

        <div class="py-12"></div>
      </section>
</template>

<script>
export default {
  data () {
    return {
      windowSize: true,
      articles: [
        {
          src: require('../assets/img/caffe1.jpg'),
          title: 'Mobile first & Responsive',
          text: 'Phasellus lorem enim, luctus ut velit eget, convallis egestas eros. Sed ornare ligula eget tortor tempor, quis porta tellus dictum.'
        },
        {
          src: require('../assets/img/caffe2.jpg'),
          title: 'Think outside the box',
          text: 'Nam ut leo ipsum. Maecenas pretium aliquam feugiat. Aenean vel tempor est, vitae tincidunt risus. Sed sodales vestibulum nibh.'
        },
        {
          src: require('../assets/img/caffe3.jpg'),
          title: 'Small changes, big difference',
          text: 'Vestibulum in dictum velit, in rhoncus nibh. Maecenas neque libero, interdum a dignissim in, aliquet vitae lectus. Phasellus lorem enim, luctus ut velit eget.'
        }
      ]
    }
  },
  mounted () {
    this.onResize()
  },
  methods: {
    onResize () {
      const w = window.innerWidth
      const h = window.innerHeight
      // console.log(w, h)
      if (w < 600 || h < 500) {
        this.windowSize = false
      } else {
        this.windowSize = true
      }
      // console.log(this.windowSize)
    }
  }
}
</script>

<style>

</style>
