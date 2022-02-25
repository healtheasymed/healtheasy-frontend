<template>
  <div id="box-especialidades">
    <template v-for="especialidade in especialidades" :key="especialidade.id">
      <CardEspecialidade :especialidade="especialidade" />
    </template>
  </div>
</template>

<script>
import { especialidades } from "@/static/landing-page";
import CardEspecialidade from "@/components/landing/elements/CardEspecialidade";

export default {
  name: "BoxEspecialidade",

  components: {
    CardEspecialidade,
  },

  data() {
    return {
      especialidades: especialidades,
    };
  },
};
</script>

<style scoped>
#box-especialidades {
  background: var(--white);
  border-radius: 10px;
  box-shadow: 0px 10px 20px rgba(41, 41, 42, 0.07);
  bottom: -5vh;
  position: relative;

  align-items: center;
  display: grid;
  gap: 40px;
  grid-template-columns: repeat(4, 1fr);
  margin-inline: auto;
  max-width: 1200px;
  min-height: 30vh;
  padding: 40px;
  place-content: center;
  place-items: center;
  row-gap: 20px;
}

/* @media (max-width: 1200px) {
  #box-especialidades {
    max-width: 1000px;
  }
}

@media (max-width: 1024px) {
  #box-especialidades {
    max-width: 800px;
  }
}

@media (max-width: 768px) {
  #box-especialidades {
    grid-template-columns: repeat(3, 1fr);
    height: auto;
    max-width: 600px;
    padding: 10px 0;
  }
}

@media (max-width: 425px) {
  #box-especialidades {
    grid-template-columns: repeat(2, 1fr);
    max-width: 300px;
  }
} */
</style>
