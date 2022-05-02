<template>
  <!-- footer in basso -->
  <section class="container px-5">
    <div class="row align-items-center py-4 my-footer-b">
      <!-- scritta copyright -->
      <div class="col">
        <p class="text-secondary">
          © 2022 Landrick. Design with
          <i class="fa fa-heart text-danger"></i> by Shreethemes.
        </p>
      </div>
      <!-- fine scritta copyright -->
      <!-- carte di credito -->
      <div class="col d-flex justify-content-end">
        <img
          class="ms-2"
          v-for="(card, index) in paymentCards"
          :key="index"
          :src="require(`../assets/img/${card.logo}`)"
          :alt="card.name"
        />
      </div>
      <!-- fine carte di credito -->
      <!-- bottone posizionato a destra -->
      <a
        class="my-btn d-flex align-items-center justify-content-center"
        href="#"
      >
        <i class="fa-solid fa-arrow-up"></i>
      </a>
      <!-- fine bottone posizionato a destra -->
    </div>
  </section>
  <!-- fine footer in basso -->
</template>

<script>
export default {
  name: "FooterBottom",
  data: function () {
    return {
      /* array carte di credito */
      paymentCards: [
        {
          name: "American-Ex card",
          logo: "american-ex.png",
        },
        {
          name: "Discover card",
          logo: "discover.png",
        },
        {
          name: "Master-Card card",
          logo: "master-card.png",
        },
        {
          name: "PayPal card",
          logo: "paypal.png",
        },
        {
          name: "Visa card",
          logo: "visa.png",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.my-footer-b {
  position: relative;
  .my-btn {
    position: absolute;
    width: 40px;
    height: 40px;
    background-color: #2b48aa;
    color: #bec1c8;
    border-radius: 5px;
    right: -100px;
  }
}
img {
  height: 25px;
}
</style>
