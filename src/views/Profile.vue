<template>
  <div>
    <div class="about">
      <HeadersTitle title="Profile Page" />
      <Information />
    </div>
  </div>
</template>

<script>
export default {
  name: "Home",
  components: {
    HeadersTitle: () => import(`@/components/HeaderTitle`),
    Information: () => import(`@/components/Information`),
  },
};
</script>
