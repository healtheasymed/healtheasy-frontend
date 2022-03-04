<template>
  <section id="planos">
    <div class="content">
      <div class="titulo">
        <h2>Nossos <span>planos</span></h2>
        <p>
          Lorem ipsum is common placeholder text used to demonstrate the graphic
          elements of a document or visual presentation.
        </p>
      </div>

      <BoxPlanos />
    </div>
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
  background: linear-gradient(
    180deg,
    var(--light-green) 10%,
    var(--white) 90%
  );
}

.titulo {
  margin-bottom: 40px;
}

.titulo h2 {
  font-size: 3rem;
}

.titulo span {
  color: var(--dark-blue);
}

.titulo p {
  margin-inline: 0;
  width: 60%;
}

@media (max-width: 375px) {
  .titulo p {
    width: 100%;
  }
}
</style>
