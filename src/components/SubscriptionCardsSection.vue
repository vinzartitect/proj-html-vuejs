<template>
  <!-- SECTION card con diversi abbonamenti -->
  <section>
    <div class="container p-5 mb-5">
      <!-- testo centrale in alto -->
      <div class="row text-center">
        <div class="col">
          <h2 class="fw-bold mb-4">
            Our rates for developer from landrick team
          </h2>
          <p class="text-secondary mb-5">
            Start working with
            <span class="my-blue-text fw-bold">Landrick</span> that can provide
            everthing you need to generate <br />
            awareness, drive traffic, connect.
          </p>
        </div>
      </div>
      <!-- fine testo centrale in alto -->
      <!-- cards piani di abbonamento -->
      <div class="row mb-5">
        <div
          class="col-12 col-lg-4 mb-5"
          v-for="(card, index) in subscriptionPlans"
          :key="index"
        >
          <div class="card overflow-hidden p-4">
            <div class="card-body">
              <span
                id="plans"
                class="d-inline-block fw-bold my-blue-text my-alice-blue-bg border rounded-pill mb-3"
                >{{ card.planType }}</span
              >
              <h2 class="card-text fw-bold">{{ card.price }}</h2>
              <p class="card-text text-secondary">Per Month</p>
              <p class="card-text text-secondary">{{ card.text }}</p>
              <hr />
              <ul class="card-text p-0 mb-4">
                <li
                  class="d-flex align-items-center text-secondary fw-bold mb-2"
                  v-for="(element, index) in propertiesPlan"
                  :key="index"
                >
                  <span class="fas fa-check my-fa-check-blue me-2"></span
                  >{{ element.property }}
                </li>
              </ul>
              <div class="card-text d-flex text-center mb-3">
                <a
                  id="buy-now"
                  class="col-12 me-3 text-decoration-none p-2 text-white my-blue-bg rounded shadow-lg"
                  href="#"
                  >Buy Now</a
                >
              </div>
              <span class="card-text text-secondary"
                >*No credit card required</span
              >
            </div>
          </div>
        </div>
      </div>
      <!-- fine cards piani di abbonamento -->
      <!-- input con bottone start -->
      <div class="row text-center justify-content-center pt-5 mb-5">
        <div class="col-12 col-lg-6">
          <h2 class="fw-bold mb-4">Want to be among the first to find out?</h2>
          <p class="text-secondary mb-4">
            Start working with
            <span class="my-blue-text fw-bold">Landrick</span> that can provide
            everthing you need to generate <br />
            awareness, drive traffic, connect.
          </p>
          <form class="input-group">
            <label for="email"></label>
            <input
              type="email"
              class="form-control"
              placeholder="Email Address"
            />
            <button
              id="btn-getStarted"
              class="btn text-white btn-outline-secondary"
              type="sumbmit"
            >
              Get Started
            </button>
          </form>
        </div>
      </div>
      <!-- fine input con bottone start -->
    </div>
  </section>
  <!-- fine SECTION card con diversi abbonamenti -->
</template>

<script>
export default {
  name: "SubscriptionCardsSection",

  data: function () {
    return {
      /* array dei piani di abbonamento */
      subscriptionPlans: [
        {
          planType: "Basic",
          price: "$9.00",
          text: "All the basics for businesses that are just getting started",
          best: false,
        },
        {
          planType: "Business",
          price: "$39.00",
          text: "Better for growing businesses that want more customers.",
          best: true,
        },
        {
          planType: "Enterprise",
          price: "$79.00",
          text: "Advanced features for pros who need more customization.",
          best: false,
        },
      ],
      /* array delle caratteristiche degli abbonamenti */
      propertiesPlan: [
        {
          property: "Full Access",
        },
        {
          property: "Enhanced Security",
        },
        {
          property: "Source Files",
        },
        {
          property: "1 Domain Free",
        },
        {
          property: "Enhanced Security",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
div.card {
  border-bottom: 4px solid rgb(150, 150, 150);
  border-radius: 15px;
  transition: all 0.2s ease-in-out;

  span#plans {
    padding: 0.5rem 1.5rem;
  }
}
div.card:hover {
  transform: scale(1.05);
  border-bottom: 4px solid #2f55d4;
  box-shadow: 0 0 15px rgb(200, 200, 200);
}
button#btn-getStarted {
  background-color: #2f55d4;
}
div.card a#buy-now:hover,
button#btn-getStarted:hover {
  background-color: #2844aa;
}
</style>
