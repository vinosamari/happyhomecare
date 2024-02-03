<script>
export default {
  name: "FooterComponent",
  data: () => {
    return {
      icons: [
        'mdi-facebook',
        'mdi-twitter',
        'mdi-linkedin',
        'mdi-instagram',
      ],
    }
  }
}
</script>

<template>
  <v-footer
    padless
  >
    <v-card
      width="100%"
      flat
      tile
      class="white--text text-center px-14"
      color="rgb(6,0,104)"
    >
      <v-card-text>
        <v-btn
          v-for="icon in icons"
          :key="icon"
          class="mx-4 white--text"
          icon
        >
          <v-icon size="24px">
            {{ icon }}
          </v-icon>
        </v-btn>
      </v-card-text>

      <v-card-text class="white--text pt-0 mt-5" v-if="!$vuetify.breakpoint.mobile">
        <span class="dokdo" style="font-size: 1.5rem">Readr</span> is a project made with love by Karma Innovative
        Technologies to help interact with your documents. We use Natural Language Processing & Artificial Intelligence
        to synthesize the answers so it won't be always perfect.<br/> Use the feedback icons <span>( <v-icon
        color="rgb(6,0,104)" size="20">mdi-thumbs-up-down</v-icon> )</span> to let us know when it gets it wrong or right so
        we can refine our responses. Contributions are welcome via our <span>contributions page</span>
      </v-card-text>

      <v-divider></v-divider>

      <v-card-text class="white--text">
        {{ new Date().getFullYear() }} — <strong>Karma Innovative Technologies</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<style scoped>

</style>
