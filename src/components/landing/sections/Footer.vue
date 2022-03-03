<template>
  <footer>
    <div class="content">
      <div class="footer-sobre">
        <img src="@/assets/logos/logo-assinatura-branco.png" alt="Health Easy - Logomarca" />
        <p>
          Lorem ipsum dolor amet, consectetur adipiscing elit.
          Eget nisl nunc quam ac sed turpis volutpat. Cursus sed
          massa non nisi, placerat.
        </p>

        <div class="contato-sites">
          <SocialButton
            v-for="site in sites"
            :key="site.id"
            :iconName="site.icone"
            :link="site.link"
            :iconSize="20"
          />
        </div>
      </div>

      <div class="footer-servicos">
        <h5>Serviços</h5>
        <p>
          Lorem ipsum dolor amet, consectetur adipiscing elit.
          Eget nisl nunc quam ac sed turpis volutpat. Cursus sed
          massa non nisi, placerat.
        </p>
        <p>ícones</p>
      </div>

      <div class="footer-contato">
        <h5>Contato</h5>
        <p>
          <mdicon
            name="email"
            size="25"
          />
          hello@landify.co
        </p>
        <p>
          <mdicon
            name="phone"
            size="25"
          />
          hello@landify.co
        </p>
        <p>
          <mdicon
            name="map-marker"
            size="25"
          />
          hello@landify.co
        </p>
      </div>
    </div>

    <div class="copyright">
      <p>© 2021 - <span>Health Easy</span></p>

      <ul>
        <li>
          <a href="#">Termos & Condições</a>
        </li>
        <li>|</li>
        <li>
          <a href="#">Política de Privacidade</a>
        </li>
      </ul>
    </div>
  </footer>
</template>

<script>
import { sites } from "@/static/landing-page";
import SocialButton from "@/components/landing/elements/SocialButton";

export default {
  name: "Footer",

  components: {
    SocialButton
  },

  data () {
    return {
      sites: sites
    }
  }
}
</script>

<style scoped>
footer {
  background: var(--black);
  font-size: 1.2rem;
  min-height: 60vh;
}

.content {
  color: var(--white);
  align-items: center;
  display: grid;
  grid-gap: 20px;
  grid-template-columns: repeat(3, 1fr);
  height: 90%;
}

.footer-sobre img {
  margin-bottom: 20px;
  max-width: 200px;
}

.footer-content h5 {
  font-size: 1.4rem;
}

.contato-sites {
  align-items: center;
  display: flex;
  gap: 10px;
  margin-top: 20px;
}

.footer-servicos,
.footer-contato {
  display: flex;
  flex-direction: column;
  gap: 16px;
}

.footer-contato {
  text-align: center;
}

.footer-content,
.copyright {
  color: var(--white);
  margin-inline: auto;
  max-width: 1200px;
  opacity: 0.8;
  padding: 0 40px;
}

.copyright {
  align-items: center;
  display: flex;
  justify-content: space-between;
}

.copyright span {
  color: var(--dark-green);
}

.copyright ul {
  align-items: center;
  display: flex;
  gap: 10px;
}

.copyright ul a {
  transition: all 0.2s ease-in-out;
}

.footer-contato .mdi,
.copyright ul a:hover {
  color: var(--dark-green) !important;
}

/* @media (max-width: 1200px) {
  .footer-content,
  .copyright {
    max-width: 1000px;
  }
}

@media (max-width: 1024px) {
  .footer-content,
  .copyright {
    max-width: 800px;
  }
}

@media (max-width: 768px) {
  footer {
    height: 45vh;
    padding: 40px 0;
  }

  .footer-content,
  .copyright {
    max-width: 600px;
  }

  .copyright {
    flex-direction: column;
    gap: 10px;
  }
}

@media (max-width: 616px) {
  footer {
    height: auto;
  }

  .footer-content {
    grid-template-columns: 1fr;
    grid-template-rows: repeat(3, 1fr);
    padding: 20px;
  }

  .copyright {
    margin-top: 20px;
  }
} */
</style>
