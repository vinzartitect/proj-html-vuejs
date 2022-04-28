<template>
  <!-- SECTION key features -->
  <section>
    <div class="container p-5 mb-5">
      <!-- testo in alto con titolo -->
      <div class="row mb-5">
        <div class="col">
          <h2 class="fw-bold mb-4">Key Features</h2>
          <p class="text-secondary">
            Start Working with
            <span class="my-blue-text fw-bold">Landrick</span> that can provide
            everything you need to generate <br />
            awareness, drive traffic, connect
          </p>
        </div>
      </div>
      <!-- fine testo in alto con titolo -->
      <!-- 4 cards -->
      <div class="row">
        <div
          class="col-sm-6 col-md-6 col-lg-3 p-2"
          v-for="(card, index) in featureCards"
          :key="index"
        >
          <div class="feature-card border rounded-3 position-relative p-4">
            <div class="card-content position-relative">
              <div
                class="square-bg d-flex justify-content-center align-items-center rounded-3 mb-4"
              >
                <i :class="card.icon" class="fa-2x my-blue-text"></i>
              </div>
              <h6 class="fw-bold">{{ card.title }}</h6>
              <p class="text-secondary">
                Composed in a pseudo-Latin language which more or less
                corresponds.
              </p>
              <a class="my-blue-text text-decoration-none fw-bold" href="#"
                >Read More <i class="fas fa-angle-right"></i
              ></a>
            </div>
            <i :class="card.icon" class="bg-icons fa-9x position-absolute"></i>
          </div>
        </div>
      </div>
      <!-- fine 4 cards -->
    </div>
  </section>
  <!-- /SECTION fine key features -->
</template>

<script>
export default {
  name: "KeyFeaturesSection",
  data: function () {
    return {
      /* array delle cards */
      featureCards: [
        {
          icon: "far fa-copy",
          title: "Modular",
        },
        {
          icon: "fas fa-tv",
          title: "Responsive",
        },
        {
          icon: "far fa-image",
          title: "Customizable",
        },
        {
          icon: "fas fa-expand-arrows-alt",
          title: "Scalable",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
div.feature-card:hover {
  position: relative;
  transform: translateY(-12px);
}

div.feature-card {
  transition: all 0.3s ease-in-out;
}

div.card-content {
  z-index: 2;
}

div.feature-card:hover i.bg-icons {
  display: inline;
}

.square-bg {
  height: 60px;
  width: 60px;
  background-color: #2f55d41a;
}

i.bg-icons {
  color: aliceblue;
  top: 15px;
  right: 10px;
  display: none;
}
</style>
