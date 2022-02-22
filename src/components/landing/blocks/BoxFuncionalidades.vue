<template>
  <div id="box-funcionalidades">
    <template
      v-for="funcionalidade in funcionalidades"
      :key="funcionalidade.id"
    >
      <CardFuncionalidade :funcionalidade="funcionalidade" />
    </template>
  </div>
</template>

<script>
import { funcionalidades } from "@/static/landing-page";
import CardFuncionalidade from "@/components/landing/elements/CardFuncionalidade";

export default {
  name: "BoxFuncionalidades",

  components: {
    CardFuncionalidade,
  },

  data() {
    return {
      funcionalidades: funcionalidades,
    };
  },
};
</script>

<style scoped>
#box-funcionalidades {
  align-items: center;
  display: grid;
  gap: 20px;
  grid-template-columns: repeat(3, 1fr);
  height: auto;
  margin-inline: auto;
  max-width: 1200px;
  place-content: center;
  place-items: center;
}
</style>
