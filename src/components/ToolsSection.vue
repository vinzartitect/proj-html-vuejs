<template>
  <!-- SECTION costruzione tools -->
  <section>
    <div class="container p-5">
      <div class="row align-items-center">
        <!-- testo a sinistra -->
        <div class="col-12 col-md-6 mb-5">
          <h2 class="mb-4 fw-bold pt-3">
            Build tools and<br />extensive documention
          </h2>
          <p class="mb-4 text-secondary">
            You can combine all the Landrick templates into a single one, you
            can take a component from the Application theme and use it in
            Website.
          </p>
          <ul class="p-0 mb-5">
            <li
              class="d-flex align-items-center text-secondary mb-2"
              v-for="(element, index) in toolsList"
              :key="index"
            >
              <span class="fas fa-check my-fa-check-blue me-2"></span
              >{{ element.text }}
            </li>
          </ul>
          <a
            class="me-3 text-decoration-none p-2 text-white my-blue-bg rounded shadow"
            href="#"
            >Read More <i class="fas fa-arrow-right"></i
          ></a>
        </div>
        <!-- fine testo a sinistra -->

        <!-- immagine a destra -->
        <div class="col-12 col-md-6">
          <img class="img-fluid" src="../assets/img/1.png" alt="tools" />
        </div>
        <!-- fine immagine a destra -->
      </div>
    </div>
  </section>
  <!-- fine SECTION costruzione tools -->
</template>

<script>
export default {
  name: "ToolsSection",
  data: function () {
    return {
      //   array elementi nella lista col check
      toolsList: [
        {
          text: "Digital Marketing Solution for Tomorrow",
        },
        {
          text: "Our Talented & Experienced Marketing Agency",
        },
        {
          text: "Create your own Skin to match your brand",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
a:hover {
  background-color: #2844aa;
}
</style>
