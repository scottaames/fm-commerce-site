<template>
  <v-app dark>
    <v-app-bar app color="darkbg" height="97" flat>
      <v-img :src="Logo" max-height="25" max-width="143" />
      <v-spacer></v-spacer>
      <v-btn color="white" class="text" text to="/">Home</v-btn>
      <v-btn color="white" class="text" text to="/headphones">Headphones</v-btn>
      <v-btn color="white" class="text" text to="/speakers">Speakers</v-btn>
      <v-btn color="white" class="text" text to="/earphones">Earphones</v-btn>
      <v-spacer></v-spacer>
      <v-btn color="transparent"><v-img :src="cartIcon"></v-img></v-btn>
    </v-app-bar>
    <v-main>
      <Banner />
      <v-container>
        <nuxt />
      </v-container>
    </v-main>
    <v-footer absolute app>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
import Banner from '@/components/Banner.vue'
import Logo from '../assets/shared/desktop/logo.svg'
import cartIcon from '../assets/shared/desktop/icon-cart.svg'
export default {
  components: {
    Banner,
  },
  data() {
    return {
      Logo,
      cartIcon,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/',
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire',
        },
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js',
    }
  },
}
</script>

<style lang="scss">
.v-toolbar__content {
  max-width: 1110px !important;
  margin: auto;
  display: flex;
  align-items: center;
  padding: 0 !important;
}

.text {
  letter-spacing: 2px;
  line-height: 26px;
  font-size: 13px;
  font-family: 'Manrope', sans-serif;
  text-transform: uppercase;
  color: white;
}
.theme--light.v-btn--active:hover::before,
.theme--light.v-btn--active::before {
  background-color: transparent;
  opacity: 1 !important;
}
</style>
