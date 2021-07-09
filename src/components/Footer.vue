<template>
  <div class="footer">
    <b-icon
      v-for="(item, index) in social"
      :key="index"
      data-aos="fade-up"
      :data-aos-delay="500 * (index + 1)"
      class="social-icon"
      @click="toPage(item.url)"
      font-scale="2"
      :icon="item.icon"
    ></b-icon>
    <p class="p-eng" data-aos="flip-right" style="padding-top: 20px;">
      © Copyright © 2021 THEERAMET SAENGSIN
    </p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      social: [
        {
          icon: "instagram",
          url: "https://www.instagram.com/met.shinosuke",
        },
        {
          icon: "linkedin",
          url: "https://www.linkedin.com/in/theeramat-sangsin-289a61182/",
        },
        {
          icon: "github",
          url: "https://github.com/mamat1123",
        },
      ],
    };
  },
  methods: {
    toPage(url) {
      if (url.startsWith("http")) {
        let win = window.open(url, "_blank");
        win.focus();
      } else {
        this.$router.push(url);
      }
    },
  },
};
</script>

<style scoped>
.footer {
  margin-top: 100px;
  padding: 40px 0;
  text-align: center;

  /* border: 1px solid; */
  background: #f2f2f2;
}
.social-icon {
  margin: 0 10px;
  cursor: pointer;
}
</style>
