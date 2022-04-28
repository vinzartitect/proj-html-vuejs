<template>
  <header class="my-light-gray-bg fixed-top">
    <nav class="container px-5">
      <div class="row align-items-center d-flex justify-content-between">
        <!-- logo a sinistra -->
        <div class="col">
          <a href="#">
            <img
              class="main-logo"
              src="../assets/img/logo-dark.png"
              alt="Landrick logo"
            />
          </a>
        </div>
        <!-- fine logo a sinistra -->
        <!-- barra di navigazione centrale -->
        <div class="col">
          <ul class="d-flex justify-content-between p-0 mb-0 gap-4">
            <li
              class="list-unstyled text-uppercase fw-bold"
              v-for="(link, index) in linksNavigation"
              :key="index"
            >
              <a
                :id="index === activeLink ? 'active-link-header' : ''"
                @click="changeActiveLink(index)"
                class="d-flex align-items-center text-decoration-none gap-2"
                :href="link.url"
                >{{ link.title }}
                <i
                  v-if="link.dropdownArrow == true"
                  class="fas fa-angle-down"
                ></i
              ></a>
            </li>
          </ul>
        </div>
        <!-- fine barra di navigazione centrale -->
        <!-- lente con bottoni vari -->
        <div class="col d-none d-lg-inline-block">
          <div id="buttons-navigation" class="d-flex justify-content-end gap-3">
            <a class="btn">
              <i class="fas fa-search text-secondary"></i>
            </a>
            <a class="square-button btn shadow-sm">
              <i class="fab fa-github my-blue-text"></i>
            </a>
            <a class="square-button btn shadow-sm">
              <i class="fab fa-stack-overflow my-blue-text"></i>
            </a>
            <a class="square-button btn shadow-sm">
              <i class="fas fa-user my-blue-text"></i>
            </a>
          </div>
        </div>
        <!-- fine lente con bottoni vari -->
      </div>
    </nav>
  </header>
</template>

<script>
export default {
  name: "HeaderComp",

  data: function () {
    return {
      /* LINK in modalità attiva */
      activeLink: 1,
      /* array dei LINK della navbar centrale */
      linksNavigation: [
        {
          title: "home",
          url: "#",
          dropdownArrow: false,
        },
        {
          title: "landing",
          url: "#",
          dropdownArrow: true,
        },
        {
          title: "pages",
          url: "#",
          dropdownArrow: true,
        },
        {
          title: "docs",
          url: "#",
          dropdownArrow: true,
        },
      ],
    };
  },
  methods: {
    /* funzione che cambia il LINK della navbar portandolo in modalità attiva */
    changeActiveLink(index) {
      if (this.linksNavigation[index] !== undefined) {
        this.activeLink = index;
      }
    },
  },
};
</script>

<style lang="scss">
header {
  height: 80px;

  nav.container {
    height: 100%;

    div.row {
      height: 100%;

      ul li a {
        color: #3c4858;
      }

      ul li a:hover {
        color: #2f55d4;
      }

      div#buttons-navigation a.square-button {
        height: 40px;
        width: 40px;
        background-color: #2f55d41a;
        display: flex;
        justify-content: center;
        align-items: center;
      }

      div#buttons-navigation a.square-button:hover {
        background-color: #2f55d4;
      }

      div#buttons-navigation a.square-button:hover i {
        color: white;
      }
    }
  }
}
</style>
