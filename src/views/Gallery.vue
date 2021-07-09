<template>
  <div>
    <HeadersTitle title="Gallery Page" />
    <div class="row justify-content-center">
      <div class="col-10 row">
        <div
          class="col-lg-3 col-md-6 col-sm-12 card-fruit"
          data-aos="fade-up"
          v-for="index in 12"
          :key="index"
        >
          <div style="overflow: hidden;">
            <b-img
              @click="onClickImg(index)"
              class="img-fruit"
              :src="require(`@/assets/img/fruit-${index}.jpg`)"
              fluid
              alt="Fluid-grow image"
            ></b-img>
          </div>
        </div>
      </div>
    </div>
    <ModalImg :index="indexSelected" ref="ModalImg" />
  </div>
</template>
<script>
export default {
  name: "Gallery",
  components: {
    HeadersTitle: () => import(`@/components/HeaderTitle`),
    ModalImg: () => import(`@/components/ModalImg`),
  },
  data() {
    return {
      indexSelected: null,
    };
  },
  methods: {
    onClickImg(index) {
      this.indexSelected = index;
      this.$refs.ModalImg.show = true;
    },
  },
};
</script>
<style scoped>
.img-fruit:hover {
  transform: scale(1.1);
  overflow: hidden;
  -webkit-transition: all 0.8s ease !important;
  -moz-transition: all 0.8s ease !important;
  -ms-transition: all 0.8s ease !important;
  transition: all 0.8s ease !important;
}
.img-fruit {
  background-size: cover;
  height: 200px;
  width: 100%;
  object-fit: cover;
  cursor: pointer;
}
.card-fruit {
  margin-top: 20px;
  /* background-color: #fafafa; */
}
</style>
