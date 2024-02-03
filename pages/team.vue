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
          image: "https://cdn.vuetifyjs.com/images/profiles/marcus.jpg",
        },
        {
          name: "Akua Ama Serwah Boateng",
          role: "Administrator or Operations Manager",
          image: require("../assets/img/ghana bea67.png"),
        },
        {
          name: "Kofi Asante Osei",
          role: "Case Manager",
          image: require("../assets/img/istockphoto-481193816-170667a.jpg"),
        },
        {
          name: "Esi Darko-Amponsah",
          role: "Registered Nurse (RN)",
          image: require("../assets/img/nurses_corner1-20200827-0016.jpg"),
        },
        {
          name: "Emmanuel Kuma",
          role: "Companion Care Specialist",
          image: require("../assets/img/african-amrican-male-nurse-815844.jpeg"),
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
