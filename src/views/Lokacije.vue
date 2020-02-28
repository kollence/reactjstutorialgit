<template>
       <section id="lokacije" style="border-top: 8px solid gray;border-bottom: 8px solid gray;">
        <v-parallax
          :height="$vuetify.breakpoint.smAndDown ? 700 : 500"
          src="../assets/img/heromap2.jpg"
        >
          <v-container fill-height>
            <v-row class="text-center">
              <v-col><h2 style="text-shadow: 2px 2px 4px #000000;" class="display-2 purple--text text--accent-1 font-weight-black">LOKACIJE</h2></v-col>
            </v-row>
            <v-row justify="space-around" class="mx-auto">
              <v-col
                v-for="{i, value, title} of stats"
                :key="value"
                cols="2"
                md="3"
                class="col-lg-2 col-sm-12"
              >
              <v-hover v-slot:default="{hover}">
                <v-card @click="showMap(i)" style="cursor: pointer;" shaped :elevation="hover ? 16 : 2" :color="hover ? `rgb(224, 224, 235, 0.9)` : `rgb(224, 224, 235, 0.1)`"
                         class="mx-auto pt-6 pb-3" raised dark>
                  <div class="text-center">
                  <div :style="hover ? `color: #AB47BC` :`color: ${title}; text-shadow: 2px 2px 4px #000000;`"
                    class="display-2 font-weight-black mb-4"

                  >{{value}}</div>
                </div>
                </v-card>
              </v-hover>
              </v-col>
            </v-row>
          </v-container>
        </v-parallax>
         <v-dialog
            v-model="dialog"
            width="1100"
          >

            <v-card>
              <v-card-title
                class="headline grey lighten-2"
                primary-title
              >
                {{single.value}}
                <v-spacer></v-spacer>
                <v-btn
                  color="red"
                  text
                  @click="dialog = false"
                >
                  CLOSE
                </v-btn>
              </v-card-title>

              <v-row>
                <v-col md="5" class="ml-2">
                  <v-img class="mb-2" v-for="(s, i) in single.img" :key="i" :src="s"></v-img>
                </v-col>
                <v-col md="6">
                  <iframe :src="single.src" :width="single.w" :height="single.h" frameborder="0" style="border:0;" allowfullscreen=""></iframe>
                  <v-col class=" font-weight-black ml-3 mt-3">
                <p>Adresa: <i>{{single.adresa}}</i></p>
                <p>Radno vreme: <i> {{single.rvreme}}</i></p>
                <p>Kontakt: <i>{{single.kontakt}}</i></p>
              </v-col>
                </v-col>
                <!-- <v-col style="position: absolute;" class="col-lg-4">

              </v-col>

                <v-col  md="4" offset="4">
                <iframe :src="single.src" :width="single.w" :height="single.h" frameborder="0" style="border:0;" allowfullscreen=""></iframe>
              </v-col>-->
              </v-row>
              <v-divider></v-divider>

              <v-card-actions>
              </v-card-actions>
            </v-card>
          </v-dialog>
      </section>
</template>
<script>
export default {
  components: {
  },
  data () {
    return {
      dialog: false,
      single: { i: '', value: '', title: '' },
      stats: [
        { i: '1', value: 'DEDINJE', title: '#CE93D8', w: '550', h: '480', img: [require('../assets/img/dedinje.jpg')], adresa: 'Vladimira Gaćinovića br. 2', rvreme: 'od 08 do 20 časova', kontakt: '064/0776-255', src: 'https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2832.2741206190585!2d20.456366415534486!3d44.775216579098775!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x475a70489639c30b%3A0xc6c22a987a2636eb!2sVladimira%20Ga%C4%87inovi%C4%87a%202%2C%20Beograd!5e0!3m2!1sen!2srs!4v1582858888065!5m2!1sen!2srs' },
        { i: '2', value: 'SENJAK', title: '#CE93D8', w: '550', h: '480', img: [require('../assets/img/Senjak.jpg')], adresa: 'Koste Glavinića 5a', rvreme: 'od 08 do 20 časova', kontakt: '064/0776-257', src: 'https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2831.268041475208!2d20.441760815767484!3d44.79572578581775!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x475a701cffeb2a91%3A0x25beef0325c408ff!2sKoste%20Glavini%C4%87a%205a%2C%20Beograd!5e0!3m2!1sen!2srs!4v1582859387722!5m2!1sen!2srs' },
        { i: '3', value: 'JURIJA GAGARINA', title: '#BA68C8', w: '550', h: '450', img: [require('../assets/img/jurija.jpg'), require('../assets/img/jurija2.jpg')], adresa: 'Jurija Gagarina 30v', rvreme: 'od 08 do 22 časova', kontakt: '065/6161-486', src: 'https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2830.8887669292376!2d20.385080915767716!3d44.80345548530775!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x475a6f75dc1a5d13%3A0xf71303d0af13b4ec!2sJurija%20Gagarina%2030v%2C%20Beograd!5e0!3m2!1sen!2srs!4v1582859532342!5m2!1sen!2srs' },
        { i: '4', value: 'USTANICKA', title: '#AB47BC', w: '550', h: '480', img: [require('../assets/img/Ustanicka.jpg')], adresa: 'Ustanička 170v', rvreme: 'od 08 do 22 časova', kontakt: '064/0776-256', src: 'https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2831.8735805898386!2d20.498971115767205!3d44.78338258663192!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x475a708e1163b2e7%3A0x371f2683af775d7b!2sUstani%C4%8Dka%20170%2C%20Beograd!5e0!3m2!1sen!2srs!4v1582859655918!5m2!1sen!2srs' },
        { i: '5', value: 'ARENA', title: '#BA68C8', w: '550', h: '480', img: [require('../assets/img/Arena.jpg')], adresa: 'Bulevar Arsenija Čarnojevića 95/4b', rvreme: 'od 08 do 20 časova', kontakt: '064/0776-258', src: 'https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2830.4719063855778!2d20.416039615767954!3d44.81194998474719!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x475a6f8a0e1c5ffd%3A0x4af61f59accd0d60!2s4b%2C%20Bulevar%20Arsenija%20%C4%8Carnojevi%C4%87a%2095%2C%20Beograd%2011070!5e0!3m2!1sen!2srs!4v1582859731486!5m2!1sen!2srs' }
      ]
    }
  },
  methods: {
    showMap (id) {
      this.dialog = true
      const one = this.stats.find(single => single.i === id)
      this.single = { ...one }
    }
  }
}
</script>

<style>

</style>
