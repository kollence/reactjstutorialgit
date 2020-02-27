<template>
<div>
         <section id="about-me">
        <div class="py-12"></div>

        <v-container class="text-center">
          <v-row class="text-center">
            <v-col justify="center" v-show="windowSize " class="justify-space-around col-md-4">
            <v-img class="mx-auto" width="200" src="../assets/img/Picture1.png"></v-img>
            </v-col>
            <v-col justify="center" class="col-md-4 my-auto col-xs-12">
              <h2 class="display-2 font-weight-bold mb-3">O NAMA</h2>
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
             “SMART KAPITAL” je privredno društvo koje posluje od 2009. godine, a koje je nastalo spajanjem manjih preduzetničkih radnji od kada uspešno posluje i razvija se, a trenutno zapošljava preko 20 mladih i stručno osposobljenih  zaposlenih i obavlja delatnost na 5 ekskluzivnih lokacija u Beogradu u oblasti brokerskih poslova sa hartijama od vrednosti i berzanskom robom, u stvarnosti to predstavlja pružanje najkvalitetnije usluge menjačkih poslova, kao i dodatne usluge platnog prometa i transakcija novcem svojim klijentima i usluge “Državne Lutrije Srbije”.

    Pored toga, privredno društvo razvija i ugostiteljsku delatnost u okviru brenda “SMART CAFFE” na više lokacija u Beogradu.
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
</div>
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
