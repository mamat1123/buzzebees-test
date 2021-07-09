<template>
  <div id="app">
    <Toolbar />
    <router-view />
    <Footer />
  </div>
</template>
<script>
import Toolbar from "@/components/Toolbar";
import Footer from "@/components/Footer";
import AOS from "aos";
import "aos/src/sass/aos.scss";
export default {
  components: {
    Toolbar,
    Footer,
  },
  created() {
    AOS.init({ offset: 0, startEvent: "load", duration: 1500 });
  },
};
</script>
<style lang="sass">
$aos-distance: 40px;
@import 'aos/src/sass/aos.scss';
</style>
<style>
body {
  background: rgb(3, 3, 4);
  background: linear-gradient(
    323deg,
    rgba(3, 3, 4, 1) 0%,
    #151718 49%,
    rgba(40, 46, 50, 1) 100%
  );
}
</style>
