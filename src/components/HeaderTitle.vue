<template>
  <div class="header-title bg-white">
    <h1 class="h1-eng" data-aos="fade-up">
      {{ title }}
    </h1>
  </div>
</template>

<script>
export default {
  props: ["title"],
};
</script>

<style scoped>
.header-title {
  /* padding: 80px 0; */
  height: calc(100vh);
  border: 1px solid #e0e0e0;
  text-align: center;
  margin-bottom: 80px;
  justify-content: center;
  align-items: center;
  display: flex;
}
</style>
