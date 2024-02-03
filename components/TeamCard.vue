<script>
export default {
  name: "TeamCard",
  props:{
    member: Object,
    required: true
  }
}
</script>

<template>
  <v-card
    class="mx-auto my-5"
    max-width="434"
    rounded
  >
    <v-img
      height="100%"
      :src="require('/assets/img/colorkit.png')"
    >
      <v-row
        align="end"
        class="fill-height"
      >
        <v-col
          align-self="start"
          class="pa-0"
          cols="12"
        >
          <v-avatar
            class="profile"
            color="grey"
            size="164"
            tile
          >
            <v-img :src="member.image"></v-img>
          </v-avatar>
        </v-col>
        <v-col class="py-0">
          <v-list-item
            color="rgba(0, 0, 0, .4)"
            dark
          >
            <v-list-item-content>
              <v-list-item-title class="text-h6">
                {{member.name}}
              </v-list-item-title>
              <v-list-item-subtitle class="mb-5">{{member.role}}</v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>
        </v-col>
      </v-row>
    </v-img>
  </v-card>
</template>

<style scoped>

</style>
