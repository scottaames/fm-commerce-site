<template>
  <section class="banner">
    <v-container>
      <div class="sep"></div>
      <v-row>
        <v-col cols="6" class="white--text">
          <p class="overline" style="opacity: 0.5">New product</p>
          <p class="text-h1">xx99 mark ii headphones</p>
          <p class="text-body-1" style="opacity: 0.75">
            Experience natural, lifelike audio and exceptional build quality
            made for the passionate music enthusiast.
          </p>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<script>
import heroImg from '../assets/home/desktop/image-hero.jpg'
export default {
  props: {
    home: {
      type: Boolean,
      default: false,
    },
  },
  data() {
    return {
      heroImg,
    }
  },
}
</script>

<style lang="scss" scoped>
.banner {
  max-width: 100vw;
  width: 100%;
  padding: 0;
  margin: 0;
  max-height: 632px;
  height: 100%;
  background: #0e0e0e url('../assets/home/desktop/image-hero.jpg') no-repeat 50%
    50%;
}
.sep {
  height: 1px;
  max-width: 1110px;

  width: 100%;
  opacity: 0.2;
  background-color: white;
}
</style>
