<template>
  <div>
    <div class="row justify-content-center">
      <div class="col-10 row justify-content-between">
        <div
          class="col-xl-6 col-lg-7 col-md-12 order-2 order-lg-1 row text-white"
          style="height: fit-content;"
        >
          <div
            v-for="(info, index) in cv"
            :key="index"
            class="col-12 group-info"
            data-aos="fade-up"
          >
            <p class="p-eng key-label">{{ info.key }}</p>
            <h3 class="h3-med-eng value-text">{{ info.value }}</h3>
          </div>
        </div>
        <div
          class="col-xl-6 col-lg-5 col-md-12 order-1 order-lg-2 row"
          data-aos="fade-left"
        >
          <img class="my-img" :src="require(`@/assets/img/my-img-2.png`)" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cv: [
        {
          key: "name",
          value: "THEERAMET SAENGSIN",
        },
        {
          key: "nickname",
          value: "MET",
        },
        {
          key: "age",
          value: "23",
        },
        {
          key: "email",
          value: "theeramat1123.ts@gmail.com",
        },
        {
          key: "phone number",
          value: "0919419924",
        },
        {
          key: "address",
          value: `4/197 soi Ramkhamhaeng 40, Bangkok, Thailand 10240 `,
        },
        {
          key: "hobbies",
          value: `Running, Play surfskate, Watching Netflix`,
        },
      ],
    };
  },
};
</script>

<style scoped>
.group-info {
  /* padding: 20px; */
  text-align: end;
}
.key-label {
  display: inline;
  border-bottom: 2px solid;
}
.value-text {
  margin-bottom: 10px;
}
.my-img {
  max-height: 800px;
  object-fit: contain;
}

@media screen and (max-width: 992px) {
  .group-info {
    /* padding: 20px; */
    text-align: start;
  }
}
</style>
