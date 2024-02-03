<template>
  <v-app class="Poppins">
    <v-navigation-drawer
      v-model="drawer"
      :mini-variant="$vuetify.breakpoint.mobile ? false : miniVariant"
      :clipped="clipped"
      fixed
      app
      color="rgba(6,0,104,0.85)"
      class="white--text"
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
          class="white--text"
        >
          <v-list-item-action>
            <v-icon color="purple">{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title class="font-weight-medium">{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar
      color="#a30367"
      :clipped-left="clipped"
      fixed
      app
      class="white--text"
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" class="white--text"/>
      <v-btn
        v-if="!$vuetify.breakpoint.mobile"
        icon
        @click.stop="miniVariant = !miniVariant"
      >
        <v-icon>mdi-{{ `chevron-${miniVariant ? 'right' : 'left'}` }}</v-icon>
      </v-btn>
      <v-spacer/>

      <v-toolbar-title>Happy Home Care</v-toolbar-title>
      <v-spacer/>

    </v-app-bar>
    <v-main>
      <v-container>
        <Nuxt/>
      </v-container>
    </v-main>
    <v-navigation-drawer
      v-model="rightDrawer"
      :right="right"
      temporary
      fixed
    >
      <v-list>
        <v-list-item @click.native="right = !right">
          <v-list-item-action>
            <v-icon light>
              mdi-repeat
            </v-icon>
          </v-list-item-action>
          <v-list-item-title>Switch drawer (click me)</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <footer-component></footer-component>
  </v-app>
</template>

<script>
import FooterComponent from "../components/FooterComponent.vue";

export default {
  name: 'DefaultLayout',
  components: {FooterComponent},
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Home',
          to: '/'
        },
        {
          icon: 'mdi-head-snowflake',
          title: 'Mental Health',
          to: '/mental-health'
        },
        {
          icon: 'mdi-weight-lifter',
          title: 'Health and Wellness',
          to: '/wellness'
        },
        {
          icon: 'mdi-human-male-female-child',
          title: 'Relationships',
          to: '/relationships'
        },
        {
          icon: 'mdi-gift',
          title: 'Donate',
          to: '/donate'
        },
        {
          icon: 'mdi-account-multiple',
          title: 'Team',
          to: '/team'
        },
        {
          icon: 'mdi-face-agent',
          title: 'Contact us',
          to: '/contact'
        },

      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  }
}
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Dokdo&family=Nanum+Gothic+Coding&family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&family=Ubuntu+Mono:ital,wght@0,400;0,700;1,400;1,700&display=swap");

.ubuntu-mono {
  font-family: 'Ubuntu Mono', monospace;
}

.Natum-Gothic-Coding {
  font-family: 'Nanum Gothic Coding', monospace;
}

.Poppins {
  font-family: 'Poppins', sans-serif;
}
</style>
