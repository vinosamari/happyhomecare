<script>
export default {
  name: "FeaturesCard",
  props: {
    title: {
      type: String,
      required: true
    },
    description: {
      type: String,
      required: true
    }
  }
}
</script>

<template>
  <v-card
    class="mx-auto mt-2 mb-5"
    max-width="344"
    hover
  >
    <v-list-item>
      <v-list-item-content>
        <v-list-item-title class="font-weight-bold">{{ title }}</v-list-item-title>
        <p class="ubuntu-mono mt-5" >{{ description }}</p>
        <v-btn
          color="#a30367"
          class="white--text mt-5"
          rounded
        >
          Book an appointment
        </v-btn>
      </v-list-item-content>
    </v-list-item>

    <v-card-actions>

    </v-card-actions>
  </v-card>
</template>
<style scoped>

</style>
