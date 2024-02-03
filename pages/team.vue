<script>
import TeamCard from "../components/TeamCard.vue";

export default {
  name: "team",
  components: {TeamCard},
  data() {
    return {
      members: [
        {
          name: "Kwabena Mensah Ayivor",
          role: "Co-founder",
          image: "https://images.unsplash.com/photo-1519141266130-208390729392?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1050&q=80",
        },
        {
          name: "Akua Ama Serwah Boateng",
          role: "Co-founder",
          image: "https://images.unsplash.com/photo-1519141266130-208390729392?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1050&q=80",
        },
        {
          name: "Kofi Asante Osei",
          role: "Co-founder",
          image: "https://images.unsplash.com/photo-1519141266130-208390729392?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1050&q=80",
        },
        {
          name: "Abena Yaa Darko-Amponsah",
          role: "Co-founder",
          image: "https://images.unsplash.com/photo-1519141266130-208390729392?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1050&q=80",
        },

      ]
    }
  }
}
</script>

<template>
<v-container>
  <h1 class="text-center">Meet our wonderful Team</h1>
  <team-card v-for="(member, index) in members" :key="index" :member="member"></team-card>
</v-container>
</template>

<style scoped>

</style>
