<template>
  <b-modal v-model="show" size="xl" centered hide-footer>
    <b-carousel
      :interval="0"
      v-model="indexCarousel"
      controls
      no-hover-pause
      label-next=""
      label-prev=""
      indicators
      background="#000"
    >
      <b-carousel-slide
        v-for="index in 12"
        :key="index"
        style="padding:0px"
        :img-src="require(`@/assets/img/fruit-${index}.jpg`)"
      ></b-carousel-slide>
    </b-carousel>
  </b-modal>
</template>

<script>
export default {
  props: ["index"],
  data() {
    return {
      show: false,
      carousel: null,
    };
  },
  computed: {
    indexCarousel: {
      get() {
        return this.carousel;
      },
      set(value) {
        this.carousel = value;
      },
    },
  },
  watch: {
    index(value) {
      this.carousel = value - 1;
    },
  },
  mounted() {
    console.log(this.show);
  },
};
</script>

<style scoped>
>>> .img-fluid {
  max-width: 100%;
  height: 80vh;
  object-fit: contain;
}
</style>
