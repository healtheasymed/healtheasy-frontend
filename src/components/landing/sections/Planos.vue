<template>
  <section id="planos">
    <div class="titulo">
      <h2>Planos</h2>
      <p>
        Lorem ipsum is common placeholder text used to demonstrate the graphic
        elements of a document or visual presentation.
      </p>
    </div>

    <BoxPlanos />
  </section>
</template>

<script>
import BoxPlanos from "@/components/landing/blocks/BoxPlanos";

export default {
  name: "Planos",

  components: {
    BoxPlanos,
  },
};
</script>

<style scoped>
#planos {
  align-items: center;
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin-inline: auto;
  max-width: 1200px;
  min-height: 100vh;
  padding: 40px 0 80px;
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
