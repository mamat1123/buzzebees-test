<template>
  <div>
    <b-navbar class="toolbar">
      <b-navbar-brand @click="toPages('/')" class="text-white"
        >METT</b-navbar-brand
      >
      <b-navbar-nav>
        <b-nav-item @click="toPages('/')">
          <p class="p-toolbar">Profile</p>
        </b-nav-item>
        <b-nav-item @click="toPages('/gallery')">
          <p class="p-toolbar">Gallery</p>
        </b-nav-item>
      </b-navbar-nav>
    </b-navbar>
  </div>
</template>

<script>
export default {
  methods: {
    toPages(url) {
      this.$router.push(url);
    },
  },
};
</script>

<style scoped>
.toolbar {
  height: 80px;
  width: 100%;
  padding: 0.5rem 1rem;
  margin: 0px;
  position: fixed;
  z-index: 12;
  background-color: black;
}
.toolbar-btn {
  padding: 20px;
  cursor: pointer;
  justify-content: center;
  align-items: center;
  display: flex;
}
</style>
