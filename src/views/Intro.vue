<template>
<div>
         <section id="intro" class="grey lighten-3">
        <div class="py-12"></div>

        <v-container class="text-center">
          <v-row flex class="text-center">
            <v-col justify="center" class="justify-space-around col-md-4 col-xs-12">
            <v-img class="mx-auto" width="250" src="../assets/img/smartchange.png"></v-img>
            </v-col>
            <v-col justify="center" class="col-md-4 my-auto col-xs-12">
                          <v-img class="mx-auto" width="200" src="../assets/img/Picture1.png"></v-img>
            </v-col>
            <v-col justify="center" class="col-md-4 col-xs-12">
                          <v-img class="mx-auto mt-4" width="250" src="../assets/img/sc.png"></v-img>
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
          >U svakom trenutku na raspolaganju su vam stručni, pouzdani, mladi i ljubazni članovi našeg tima koji odgovaraju na sve vaše zahteve.

   Kontinuiranim ulaganjem u inovacije i poboljšanja u okviru svojih delatnosti “SMART KAPITAL” je već 10 godina pouzdan partner svojim klijentima, koji gradi brend i širi svoju zonu poslovanja.
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
