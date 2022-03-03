<template>
  <Header />
  <Home />
  <Especialidades />
  <Funcionalidades />
  <SobreApp1 />
  <SobreApp2 />
  <Planos />
</template>

<script>
import Header from "@/components/landing/groups/Header";
import Home from "@/components/landing/sections/Home";
import Especialidades from "@/components/landing/sections/Especialidades";
import Funcionalidades from "@/components/landing/sections/Funcionalidades";
import SobreApp1 from '@/components/landing/sections/SobreApp1';
import SobreApp2 from '@/components/landing/sections/SobreApp2';
import Planos from "@/components/landing/sections/Planos";

export default {
  name: "LandingPage",

  components: {
    Header,
    Home,
    Especialidades,
    Funcionalidades,
    SobreApp1,
    SobreApp2,
    Planos,
  },
};
</script>

<style></style>
