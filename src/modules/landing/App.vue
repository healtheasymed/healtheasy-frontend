<template>
  <Header />
  <Home />
  <Especialidades />
</template>

<script>
import Header from "@/components/landing/groups/Header";
import Home from "@/components/landing/sections/Home";
import Especialidades from "../../components/landing/groups/Especialidades";

export default {
  name: "LandingPage",

  components: {
    Header,
    Home,
    Especialidades,
  },
};
</script>

<style></style>
