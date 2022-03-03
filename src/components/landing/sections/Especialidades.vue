<template>
  <section id="especialidades">
    <div class="content">
      <div class="titulo">
        <h2>O sistema ideal para sua</h2>
        <p>especialidade médica:</p>
      </div>

      <BoxEspecialidades />
    </div>
  </section>
</template>

<script>
import BoxEspecialidades from "@/components/landing/blocks/BoxEspecialidades";

export default {
  name: "Especialidades",

  components: {
    BoxEspecialidades,
  },
};
</script>

<style scoped>
#especialidades {
  min-height: 55vh;
}

.content {
  background: var(--light-blue);
  height: 45vh;
}

.titulo p {
  color: var(--dark-blue);
}
</style>
