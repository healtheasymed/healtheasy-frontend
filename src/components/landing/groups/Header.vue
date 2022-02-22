<template>
  <header>
    <div class="header-content">
      <nav>
        <ul class="animate__animated animate__bounceInDown">
          <li class="logo-item">
            <router-link to="/#home" class="logo">
              <img src="@/assets/logos/logo-assinatura.png" alt="Health Easy" />
            </router-link>
          </li>

          <li class="menu-itens" v-for="item in menu" :key="item.id">
            <a :href="item.link">{{ item.nome }}</a>
          </li>
        </ul>
      </nav>

      <div class="header-buttons">
        <Button text="Login" @click="redirectToApp" />
      </div>
    </div>

    <div class="header-content mobile">
      <div class="header-top">
        <p @click="isMenuOpen = !isMenuOpen" class="menu-button">
          <span
            :class="`mdi mdi-${isMenuOpen ? 'close' : 'menu'}`"
            style="fontsize: 30px"
          />
        </p>

        <!-- <a href="#home" class="logo">
          <img src="@/assets/-logo.png" alt=" - Logomarca" />
        </a> -->

        <!-- <div class="header-buttons">
          <Button text="Login" @click="redirectToApp" />
        </div> -->
      </div>

      <transition name="menu-transition">
        <nav v-show="isMenuOpen">
          <ul>
            <li class="logo-item"></li>
            <li class="menu-itens" v-for="item in menu" :key="item.id">
              <a :href="item.link" @click="isMenuOpen = !isMenuOpen">{{
                item.nome
              }}</a>
            </li>
          </ul>
        </nav>
      </transition>
    </div>
  </header>
</template>

<script>
import { menu } from "@/static/landing-page";
import Button from "@/components/landing/elements/Button";

export default {
  name: "Header",

  components: {
    Button,
  },

  data() {
    return {
      menu: menu,
      isMenuOpen: false,
    };
  },

  methods: {
    redirectToApp() {
      window.location.href = window.location.origin + "/app";
    },
  },
};
</script>

<style scoped>
header {
  background: var(--white);
  border-bottom: 1px solid var(--gray);
  min-height: 8vh;
  padding: 20px 0;
  position: sticky;
  top: 0px;
  z-index: 999;
}

.header-content {
  align-items: center;
  display: flex;
  height: 100%;
  justify-content: space-between;
  margin-inline: auto;
  max-width: 1200px;
}

.header-content.mobile {
  display: none;
}

.header-content nav ul {
  align-items: center;
  display: flex;
  gap: 40px;
}

.logo img {
  width: 200px;
}

.header-content nav a:not(.logo) {
  color: var(--black);
  font-size: 1.2rem;
  font-weight: 500;
  position: relative;
}

.header-content nav li:nth-child(2) a {
  font-weight: 600;
}

.header-content nav a:before {
  background: var(--dark-blue);
  bottom: 0;
  content: "";
  height: 0;
  left: -10px;
  position: absolute;
  transition: all 0.3s ease-in-out;
  visibility: hidden;
  width: 100%;
}

nav a:hover:not(.logo):before {
  height: 1px;
  left: 0;
  visibility: visible;
}

.header-buttons {
  display: flex;
  gap: 20px;
}

@media (max-width: 1200px) {
  .header-content {
    max-width: 1000px;
  }
}

@media (max-width: 1024px) {
  .header-content {
    max-width: 800px;
  }
}

@media (max-width: 768px) {
  .header-content {
    max-width: 600px;
  }

  .header-content nav ul {
    gap: 10px;
  }
}

@media (max-width: 616px) {
  .header-content:not(.mobile) {
    display: none;
  }

  .header-content.mobile {
    display: flex;
    position: relative;
  }

  .header-top {
    align-items: center;
    display: flex;
    justify-content: space-between;
    padding: 0 20px;
    width: 100%;
  }

  .menu-button {
    cursor: pointer;
    z-index: 10;
  }

  .menu-transition-enter-active {
    transition: all 0.4s ease;
  }

  .menu-transition-leave-active {
    transition: all 0.2s cubic-bezier(1, 0.5, 0.8, 1);
  }

  .menu-transition-enter,
  .menu-transition-leave-to {
    opacity: 0;
    transform: translateX(10px);
  }

  .header-content.mobile nav {
    background: var(--white);
    height: 100vh;
    position: absolute;
    top: 0;
    width: 60vw;
  }

  .header-content.mobile nav ul {
    flex-direction: column;
    padding: 10vh 0;
    gap: 40px;
  }

  .header-content nav a:not(.logo) {
    font-size: 1.8rem;
  }
}
</style>
