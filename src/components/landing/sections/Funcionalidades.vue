<template>
  <section id="funcionalidades">
    <div class="titulo">
      <h2>Funcionalidades</h2>
      <p>
        Lorem ipsum is common placeholder text used to demonstrate the graphic
        elements of a document or visual presentation.
      </p>
    </div>

    <BoxFuncionalidades />
  </section>
</template>

<script>
import BoxFuncionalidades from "@/components/landing/blocks/BoxFuncionalidades";

export default {
  name: "Funcionalidades",

  components: {
    BoxFuncionalidades,
  },
};
</script>

<style scoped>
#funcionalidades {
  align-items: center;
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin-inline: auto;
  max-width: 1200px;
  min-height: 70vh;
}

.titulo {
  margin-bottom: 5vh;
  text-align: center;
}

.titulo h2 {
  color: var(--dark-blue);
  font-weight: 700;
  font-size: 2.6rem;
  margin-bottom: 10px;
}

.titulo p {
  font-size: 1.2rem;
  line-height: 1.4;
  margin-inline: auto;
  width: 60%;
}
</style>
