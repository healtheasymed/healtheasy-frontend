<template>
  <section id="sobre2">
    <div class="sobre2-content">
      <div class="section-left">
        <h1>Agenda médica na palma da mão</h1>

        <p>
          Com a agenda médica online do <b>Health Easy</b>, sua equipe controla
          agendamentos, diminui faltas por meio do envio de SMS e e-mail e ganha
          tempo para realizar o que realmente importa: o atendimento ao
          paciente.
        </p>
        <p>
          Com a agenda médica online do <b>Health Easy</b>, sua equipe controla
          agendamentos.
        </p>

        <div class="left-chips">
          <Chip
            title="+ de 10 milhões"
            subtitle="de atendimentos."
            bgColor="var(--light-green)"
            titleColor="var(--dark-blue)"
            :height="50"
            :width="200"
          />

          <Chip
            title="+ de 10 milhões"
            subtitle="de atendimentos."
            bgColor="var(--light-green)"
            titleColor="var(--dark-blue)"
            :height="50"
            :width="200"
          />
        </div>
      </div>

      <div class="section-right">
        <ImageBG bgColor="var(--dark-blue)" />
      </div>
    </div>
  </section>
</template>

<script>
import Chip from "@/components/landing/elements/Chip";
import ImageBG from "@/components/landing/elements/ImageBG";

export default {
  name: "SobreApp2",

  components: {
    Chip,
    ImageBG,
  },
};
</script>

<style scoped>
#sobre2 {
  background: var(--light-blue);
  color: var(--primary-text);
  padding: 40px 0;
}

.sobre2-content {
  align-items: center;
  display: grid;
  grid-auto-flow: dense;
  grid-gap: 20px;
  grid-template-columns: repeat(2, 1fr);
  margin-inline: auto;
  max-width: 1200px;
  min-height: 70vh;
}

.section-left {
  display: flex;
  flex-direction: column;
  gap: 20px;
  grid-column: 2;
  width: 90%;
}

.section-left h1 {
  color: var(--dark-blue);
  font-size: 3rem;
}

.section-left p {
  font-size: 1.2rem;
}

.left-chips {
  display: flex;
  gap: 40px;
  margin-top: 2rem;
}

.section-left b {
  color: var(--dark-blue);
}

.section-right {
  height: 100%;
  position: relative;
  width: 90%;
}

.section-right img {
  display: block;
  max-width: 100%;
}

/* @media (max-width: 1200px) {
  .sobre2-content {
    max-width: 1000px;
  }
}

@media (max-width: 1024px) {
  .sobre2-content {
    max-width: 800px;
  }

  .section-left h1 {
    font-size: 3.8rem;
  }
}

@media (max-width: 768px) {
  .sobre2-content {
    grid-template-columns: 1fr;
    grid-template-rows: repeat(2, 1fr);
    max-width: 600px;
    padding: 40px 0;
  }

  .section-left {
    align-items: center;
    grid-row: 2;
    text-align: center;
  }

  .section-left h1 {
    font-size: 3.4rem;
  }
}

@media (max-width: 548px) {
  .sobre2-content {
    grid-template-rows: 1fr;
  }
}

@media (max-width: 375px) {
  .section-right {
    width: 60%;
  }
} */
</style>
