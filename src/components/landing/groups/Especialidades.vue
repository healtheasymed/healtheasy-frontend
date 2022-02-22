<template>
  <section id="especialidades">
    <div class="especialidades-content">
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
  min-height: 65vh;
}

.especialidades-content {
  background: var(--light-blue);
  height: 45vh;
  padding-top: 8vh;
  width: 100%;
}

.titulo {
  font-weight: 700;
  font-size: 2rem;

  margin-inline: auto;
  max-width: 1200px;
}

.titulo p {
  color: var(--dark-blue);
}
</style>
