<template>
  <Header />
  <Home />
  <Especialidades />
  <Funcionalidades />
</template>

<script>
import Header from "@/components/landing/groups/Header";
import Home from "@/components/landing/sections/Home";
import Especialidades from "@/components/landing/groups/Especialidades";
import Funcionalidades from "@/components/landing/groups/Funcionalidades";

export default {
  name: "LandingPage",

  components: {
    Header,
    Home,
    Especialidades,
    Funcionalidades,
  },
};
</script>

<style></style>
