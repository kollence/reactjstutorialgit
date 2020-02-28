<template>
      <section
        id="smart-change"
        class="grey lighten-3"
        style="background-color: rgb(0,0,0, 0.7)"
      >
      <!-- <v-parallax
          :height="$vuetify.breakpoint.smAndDown ? 700 : 1900"
          src="../assets/img/pbg.jpg"
        > -->
       <v-row>
            <v-col justify="center" v-show="windowSize " class="justify-space-around col-md-4">
            <v-img class="mx-auto" width="300" src="../assets/img/smartchange.png"></v-img>
            </v-col>
            <v-col justify="center" class="text-center col-md-4 my-auto col-xs-12">
              <h2 class="display-2 black--text font-weight-bold mb-3">SMART CHANGES</h2>
            </v-col>
            <v-col justify="center" v-show="windowSize" class="col-md-4">
            </v-col>
          </v-row>
          <v-responsive
            class="mx-auto mb-1"
            width="56"
          >
            <v-divider class="mb-1"></v-divider>

            <v-divider></v-divider>
          </v-responsive>
        <v-container class="text-center">

          <v-row style="position: relative;">
              <v-col class="col-sm-2 col-md-4 text-right" >
            <v-avatar style="border: black 4px solid"
                      size="140"
                    >
                      <v-img
                        src="../assets/img/ljubaznoosoblje.jpeg"
                      ></v-img>
                    </v-avatar>
            </v-col>
            <v-col class="col-sm-10 col-md-8 text-left" align-self="center">
              <h3 class="amber--text text--accent-3">LJUBAZNO I PROFESIONALNO OSOBLJE</h3>
            </v-col>

            <v-col class="col-md-8 col-sm-10 mt-n12 text-right" align-self="center" >
              <h3 class="amber--text text--accent-3">10 GODINA POSTOJANJA</h3>
            </v-col>
            <v-col  class="col-sm-2 mt-n12 text-left col-md-4">
              <v-avatar style="border: black 4px solid"
                      size="140"
                    >
                      <v-img
                        src="../assets/img/10.jpeg"
                      ></v-img>
                    </v-avatar>
            </v-col>

            <v-col class="col-sm-2 mt-n12 col-md-4 text-right">
               <v-avatar style="border: black 4px solid"
                      size="140"
                    >
                      <v-img
                        src="../assets/img/stimulativnikursevi.jpg"
                      ></v-img>
                    </v-avatar>
              </v-col>
              <v-col class="col-sm-10 mt-n12 col-md-8 text-left" align-self="center">
               <h3 class="amber--text text--accent-3">STIMULATIVNI KURS</h3>
              </v-col>
            <v-col class="col-sm-10 mt-n12 col-md-8 text-right"  align-self="center">
              <h3 class="amber--text text--accent-3">BRZA I EFIKASNA USLUGA</h3>
            </v-col>
            <v-col class="col-sm-2 mt-n12 col-md-4 text-left">
                <v-avatar style="border: black 4px solid"
                      size="140"
                    >
                      <v-img
                        src="../assets/img/faf2.jpg"
                      ></v-img>
                    </v-avatar>
            </v-col>
             <v-col class="col-sm-2 mt-n12 col-md-4 text-right">
               <v-avatar style="border: black 4px solid"
                      size="140"
                    >
                      <v-img
                        src="../assets/img/du.png"
                      ></v-img>
                    </v-avatar>
              </v-col>
              <v-col class="col-sm-10 mt-n12 col-md-8 text-left" align-self="center">
               <h3 class="amber--text text--accent-3">VELIKI BROJ DODATNIH USLUGA</h3>
              </v-col>
              <v-col class="col-sm-10 mt-n12 col-md-8 text-right" align-self="center">
               <h3 class="amber--text text--accent-3">MREZA MENJACNICA NA 5 EKSKLUZIVNIH</h3>
               <h3 class="pt-0 mt-0 amber--text text--accent-3">LOKACIJA U BEOGRADU</h3>
              </v-col>
              <v-col class="col-sm-2 mt-n12 col-md-4 text-left">
               <v-avatar style="border: black 4px solid"
                      size="140"
                    >
                      <v-img
                        src="../assets/img/faf.jpg"
                      ></v-img>
                    </v-avatar>
              </v-col>
               <v-col class="col-sm-2 mt-n12 col-md-4 text-right">
               <v-avatar style="border: black 4px solid"
                      size="140"
                    >
                      <v-img
                        src="../assets/img/luck.jpg"
                      ></v-img>
                    </v-avatar>
              </v-col>
              <v-col class="col-sm-10 mt-n12 col-md-8 text-left" align-self="center">
               <h3 class="amber--text text--accent-3">DRZAVNA LUTRIJA SRBIJE</h3>
              </v-col>
              <v-col class="col-sm-10 mt-n12 col-md-8 text-right" align-self="center">
               <h3 class="amber--text text--accent-3">UPLATA RACUNA</h3>
              </v-col>
              <v-col class="col-sm-2 mt-n12 col-md-4 text-left">
               <v-avatar style="border: black 4px solid"
                      size="140"
                    >
                      <v-img
                        src="../assets/img/ur.jpg"
                      ></v-img>
                    </v-avatar>
              </v-col>
              <v-col class="col-sm-2 mt-n12 col-md-4 text-right">
               <v-avatar style="border: black 4px solid"
                      size="140"
                    >
                      <v-img
                        src="../assets/img/loyalty.png"
                      ></v-img>
                    </v-avatar>
              </v-col>
              <v-col class="col-sm-10 mt-n12 col-md-8 text-left" align-self="center">
               <h3 class="amber--text text--accent-3">LOYALITY KARTICE</h3>
              </v-col>
          </v-row>
          <v-responsive
            class="mx-auto mb-12"
            width="56"
          >
            <v-divider class="mb-1"></v-divider>

            <v-divider></v-divider>
          </v-responsive>
        </v-container>

        <div class="py-12"></div>
      <!-- </v-parallax> -->
      </section>
</template>

<script>
export default {
  name: 'SmartChanges',
  data () {
    return {
      windowSize: true
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
