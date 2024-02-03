<template>
  <v-row justify="center" align="center">
    <v-col cols="12" align-self="center">
      <img src="../assets/img/logo.png" alt="logo" :width="$vuetify.breakpoint.mobile ? '100%' : '50%'" class="mx-auto" height="320"/>
      <v-carousel :show-arrows="false" cycle height="70vh" hide-delimiter-background>
        <v-carousel-item v-for="(item, i) in items" :key="i" :src="item.src">
          <v-container fill-height fluid>
            <v-row align="center" justify="center" class="fill-height">
              <v-col>
                <v-row justify="center" align="center" class="fill-height">
                  <v-col>
                    <v-card class="text-center mx-auto" color="rgba(255,255,255,0.5)" elevation="3" :width="$vuetify.breakpoint.mobile ? '70%' : '40%'" >
                      <v-card-text class="black--text font-weight-bold elevation-2 px-5" style="font-size: 1.3rem">{{item.text}}</v-card-text>
                    </v-card>
                  </v-col>
                </v-row>
              </v-col>
            </v-row>
          </v-container>
        </v-carousel-item>
      </v-carousel>
      <v-card rounded elevation="3">
        <v-card-title id="#services" class="font-weight-bold text-uppercase">Our services</v-card-title>
        <features-card v-for="(feature, index) in services" :key="index" :title="feature.title" :description="feature.text"></features-card>
      </v-card>
    </v-col>
  </v-row>

</template>

<script>
import FeaturesCard from "../components/FeaturesCard.vue";

export default {
  name: 'IndexPage',
  components: {FeaturesCard},
  head:{
    title: 'Home'
  },
  data() {
    return {
      items: [
        {
          src: require('../assets/img/IMG8.jpg'),
          text: "Caring Hearts, Compassionate Care: Where Elders Become Family."
        },
        {
          src: require('../assets/img/IMG7.png'),
          text: "Nurturing Smiles, Creating Bonds: Your Trusted Elderly Care Partner."
        },
        {
          src: require('../assets/img/IMG6.jpg'),
          text: "Dignity in Every Detail: Providing Exceptional Care for Seniors.\""
        },
        {
          src: require('../assets/img/IMG9.jpg'),
          text: "Cherishing Moments, Embracing Lives: A Home for Elderly Happiness."
        },
        {
          src: require('../assets/img/IMG5.jpeg'),
          text: "Warmth Beyond Words: Crafting a Legacy of Love for Our Elders."
        },



      ],
      services:[
        {
          'title': 'Personal Care Assistance:',
          'text': 'Providing support with activities of daily living, such as bathing, grooming, dressing, and assistance with mobility to ensure clients\' comfort and well-being.'
        },
        {
          'title': 'Companion Care Services:',
          'text': 'Offering companionship, social interaction, and emotional support through engaging activities, conversation, and accompaniment to appointments or outings.'
        },
        {
          'title': 'Medication Management:',
          'text': 'Ensuring proper administration of medications, adherence to prescribed schedules, and monitoring for any potential side effects or complications, with the aim of promoting health and safety for the clients.'
        },

      ]
    }
  }
}
</script>
