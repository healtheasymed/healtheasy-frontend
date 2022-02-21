<template>
  <section id="home">
    <div class="home-content">
      <div class="section-left animate__animated animate__backInLeft">
        <h1>Sistema para clínicas e consultórios médicos</h1>

        <p>Junte-se a médicos de todo o Brasil e transforme sua gestão com o <b>Health Easy</b>. Da agenda online à gestão financeira, ganhe tempo e lucratividade na rotina de sua clínica ou consultório médico.</p>

        <Button
          text="Entrar em contato"
          :height="50"
          :width="200"
          link="#contato"
        />
      </div>

      <div class="section-right animate__animated animate__backInRight">
        <!-- TODO: trocar imagem -->
        <img src="@/assets/mockup-1.jpg" alt="" />
      </div>
    </div>
  </section>
</template>

<script>
import Button from "@/components/landing/elements/Button";

export default {
  name: "HomeSection",

  components: {
    Button,
  },
};
</script>

<style scoped>
#home {
  background: var(--white);
  color: var(--primary-text);
  padding: 40px 0;
}

.home-content {
  align-items: center;
  display: grid;
  grid-gap: 20px;
  grid-template-columns: repeat(2, 1fr);
  margin-inline: auto;
  max-width: 1200px;
}

.section-left {
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.section-left h1 {
  color: var(--dark-blue);
  font-size: 3rem;
}

.section-left p {
  font-size: 1.2rem;
}

.section-left b {
  color: var(--dark-blue);
}

.section-right {
  margin-inline: auto;
}

.section-right img {
  display: block;
  max-width: 100%;
}

@media (max-width: 1200px) {
  .home-content {
    max-width: 1000px;
  }
}

@media (max-width: 1024px) {
  .home-content {
    max-width: 800px;
  }

  .section-left h1 {
    font-size: 3.8rem;
  }
}

@media (max-width: 768px) {
  .home-content {
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
  .home-content {
    grid-template-rows: 1fr;
  }
}

@media (max-width: 375px) {
  .section-right {
    width: 60%;
  }
}
</style>
