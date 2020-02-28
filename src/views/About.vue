<template>
        <section id="blog">
        <div class="py-12"></div>
<v-row class="text-center">
            <v-col justify="center" class="text-center col-md-12 my-auto col-xs-12">
              <h2 class="display-2 font-weight-bold mb-3">Misija, Vizija, Cilj</h2>
            </v-col>
          </v-row>
        <v-container>
          <h2 class="display-2 font-weight-bold mb-3 text-uppercase text-center"></h2>

          <v-responsive
            class="mx-auto mb-12"
            width="56"
          >
            <v-divider class="mb-1"></v-divider>

            <v-divider></v-divider>
          </v-responsive>

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

              <h3
                class="font-weight-black mb-4 text-uppercase"
                v-text="title"
              ></h3>

              <div
                class="title font-weight-light mb-5"
                v-text="text"
              ></div>
            </v-col>
          </v-row>
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
          src: 'https://images.unsplash.com/photo-1423784346385-c1d4dac9893a?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1950&q=80',
          title: 'Naša misija',
          text: 'Naša misija je da pametnim odlukama kreiramo snažan i održivi sistem koji će uspesno realizovati sve finansijske ciljeve naših klijenata. Stvaramo sigurne, efikasne i iznad svega pouzdane finansijske usluge u saradnji sa odgovornim i kvalitetnim ljudima'
        },
        {
          src: 'https://images.unsplash.com/photo-1475938476802-32a7e851dad1?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1950&q=80',
          title: 'Naša vizija',
          text: 'Želimo da budemo moderna kompanija koja stalno napreduje i ulaže u inovacije i tehnološki napredak u želji da pokažemo pravac u kom se nezaustavljivo krećcemo'
        },
        {
          src: 'https://images.unsplash.com/photo-1416339442236-8ceb164046f8?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1892&q=80',
          title: 'Naš cilj',
          text: 'Kreiranje snažan i održiv sistem i postati neprikosnoveni lider na finansijskom tržištu'
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
      ]

    }
  }

}
</script>
