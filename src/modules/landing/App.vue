<template>
  <Header />
  <Home />
</template>

<script>
import Header from "@/components/landing/blocks/Header.vue";
import Home from "@/components/landing/sections/Home.vue";

export default {
  name: "LandingPage",

  components: {
    Header,
    Home
  },
};
</script>

<style></style>
