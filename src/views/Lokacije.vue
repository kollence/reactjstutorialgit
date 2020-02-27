<template>
       <section id="stats">
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
                v-for="[value, title] of stats"
                :key="value"
                cols="2"
                md="3"
                class="col-lg-2 col-sm-12"
              >
                <div class="text-center">
                  <div :style="`color: ${title}; text-shadow: 2px 2px 4px #000000;`"
                    class="display-2 font-weight-black mb-4"

                  >{{value}}</div>
                </div>
              </v-col>
            </v-row>
          </v-container>
        </v-parallax>
      </section>
</template>

<script>
export default {
  data () {
    return {
      stats: [
        ['DEDINJE', '#CE93D8'],
        ['SENJAK', '#CE93D8'],
        ['ARENA', '#BA68C8'],
        ['USTANICKA', '#AB47BC'],
        ['JURIJA GAGARINA', '#BA68C8']
      ]
    }
  }
}
</script>

<style>

</style>
