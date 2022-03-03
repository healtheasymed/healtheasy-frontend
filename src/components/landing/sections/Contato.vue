<template>
  <section id="contato" ref="contato">
    <div class="content">
      <div class="titulo">
        <h2>Entre em <span>contato</span></h2>
        <p>
          Lorem ipsum is common placeholder text used to demonstrate
          the graphic elements of a document or visual presentation.
        </p>

        <div class="contato-sites">
          <SocialButton
            v-for="site in sites"
            :key="site.id"
            :iconName="site.icone"
            :link="site.link"
            isColored
          />
        </div>
      </div>

      <FormContato />
    </div>
  </section>
</template>

<script>
import { sites } from "@/static/landing-page";
import SocialButton from "@/components/landing/elements/SocialButton";
import FormContato from "@/components/landing/groups/FormContato";

export default {
  name: "Contato",

  components: {
    SocialButton,
    FormContato
  },

  data () {
    return {
      sites: sites
    }
  }
}
</script>

<style scoped>
#contato {
  background: var(--light-blue);
  height: auto;
  min-height: 80vh;
}

.content {
  align-items: center;
  display: grid;
  grid-gap: 20px;
  grid-template-columns: repeat(2, 1fr);
  height: 100%;
  margin-inline: auto;
  max-width: 1200px;
  padding: 40px 0;
}

.titulo {
  text-align: center;
}

.titulo h2 {
  font-weight: 700;
  font-size: 3rem;
  margin-bottom: 30px;
}

.titulo span {
  color: var(--dark-green);
}

.titulo p {
  font-size: 1.2rem;
  line-height: 1.6;
  margin-bottom: 30px;
  margin-inline: auto;
  text-align: left;
  width: 80%;
}

.contato-sites {
  align-items: center;
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  justify-content: center;
}

/* @media (max-width: 1024px) {
  #contato {
    height: 60vh;
  }
}

@media (max-width: 768px) {
  #contato {
    height: auto;
  }

  .contato-content {
    gap: 0;
    grid-template-columns: 1fr;
    grid-template-rows: 1fr;
    max-width: 600px;
    padding-bottom: 40px;
  }
} */
</style>
