<template>
           <section id="usluge">
        <div class="py-12"></div>

        <v-container class="text-center">
          <v-row>
            <v-col justify="center" v-show="windowSize " class="justify-space-around col-md-4">
            <!-- <v-img class="mx-auto" width="200" src="../assets/img/Picture1.png"></v-img> -->
            </v-col>
            <v-col justify="center" class="text-center col-md-4 my-auto col-xs-12">
              <h2 class="display-2 font-weight-bold mb-3">USLUGE</h2>
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
            U mreži naših menjačnica nudimo:
Povoljne kusreve uz mogućnost dogovora za zamenu svih svetskih valuta. Brza i pouzdana transakcija bilo koje vrednosti

Dodatne usluge

          </v-responsive>
            <v-responsive>
                <v-row>
                    <v-col class="col-lg-3">
                        <v-img src="../assets/img/wu.png"></v-img>
                    </v-col>
                    <v-col class="col-lg-3">
                        <v-img src="../assets/img/dls.png"></v-img>
                    </v-col>
                    <v-col class="col-lg-3">
                        <v-img src="../assets/img/mg.png"></v-img>
                    </v-col>
                    <v-col class="col-lg-3">
                        <v-img src="../assets/img/platnip.png"></v-img>
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

<style>

</style>
