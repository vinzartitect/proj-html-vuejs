<template>
  <!-- footer in alto con menu nav -->
  <section>
    <div class="container p-5">
      <div class="row">
        <!-- loghi social -->
        <div class="col-6 col-md-3">
          <a href="#">
            <img
              class="main-logo mb-4"
              src="../assets/img/logo-light.png"
              alt="Landrick logo"
            />
          </a>
          <p class="text-secondary mb-4">
            Start working with Landrick that can provide everthing you need to
            generate awareness, drive traffic, connect.
          </p>
          <div id="socials">
            <a
              v-for="(social, index) in socialsList"
              :key="index"
              :href="social.URL"
              :class="social.logo"
              class="me-2 fa-2x"
            ></a>
          </div>
        </div>
        <!-- fine loghi social -->

        <!-- vari link menu -->
        <div class="col-6 col-md-3">
          <h5 class="text-white mb-4">Company</h5>
          <ul class="p-0">
            <li
              class="list-unstyled mb-2"
              v-for="(link, index) in companyListLinks"
              :key="index"
            >
              <i class="fas fa-angle-right text-secondary me-2"></i
              ><a
                class="text-decoration-none text-secondary"
                :href="link.URL"
                >{{ link.name }}</a
              >
            </li>
          </ul>
        </div>
        <div class="col-6 col-md-3">
          <h5 class="text-white mb-4">Usefull Links</h5>
          <ul class="p-0">
            <li
              class="list-unstyled mb-2"
              v-for="(link, index) in usefullLinks"
              :key="index"
            >
              <i class="fas fa-angle-right text-secondary me-2"></i
              ><a
                class="text-decoration-none text-secondary"
                :href="link.URL"
                >{{ link.name }}</a
              >
            </li>
          </ul>
        </div>
        <!-- fine vari link menu -->

        <!-- newsletter -->
        <div class="col-6 col-md-3">
          <h5 class="text-white mb-4">Newsletter</h5>
          <p class="text-secondary">
            Sign up and receive the latest tips via email.
          </p>
          <p class="text-secondary fw-bold">
            Write your email <span class="text-danger">*</span>
          </p>
          <form class="row input-group g-3">
            <label for="email"></label>
            <input
              type="email"
              id="inputEmail"
              class="form-control text-white"
              placeholder="Your email:"
            />
            <button type="submit" id="btn-subscribe" class="btn">
              Subscribe
            </button>
          </form>
        </div>
        <!-- fine newsletter -->
      </div>
    </div>
  </section>
  <!-- fine footer in alto con menu nav -->
</template>

<script>
export default {
  name: "FooterNav",
  data: function () {
    return {
      /* array company */
      companyListLinks: [
        {
          name: "About us",
          URL: "#",
        },
        {
          name: "Services",
          URL: "#",
        },
        {
          name: "Team",
          URL: "#",
        },
        {
          name: "Pricing",
          URL: "#",
        },
        {
          name: "Project",
          URL: "#",
        },
        {
          name: "Careers",
          URL: "#",
        },
        {
          name: "Blog",
          URL: "#",
        },
        {
          name: "Login",
          URL: "#",
        },
      ],
      /* array usefull */
      usefullLinks: [
        {
          name: "Terms of Services",
          URL: "#",
        },
        {
          name: "Privacy Policy",
          URL: "#",
        },
        {
          name: "Documentation",
          URL: "#",
        },
        {
          name: "Changelog",
          URL: "#",
        },
        {
          name: "Components",
          URL: "#",
        },
      ],
      /* array social */
      socialsList: [
        {
          logo: "fab fa-facebook-square",
          URL: "#",
        },
        {
          logo: "fab fa-instagram-square",
          URL: "#",
        },
        {
          logo: "fab fa-twitter-square",
          URL: "#",
        },
        {
          logo: "fab fa-linkedin",
          URL: "#",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
section {
  border-bottom: 1px solid rgba(255, 255, 255, 0.1);
  input#inputEmail {
    background-color: #27314f;
    border: #27314f;
  }
  button#btn-subscribe {
    background-color: #222e51;
    color: #2844aa;
    box-shadow: 0 0 3px #2844aa;
  }
  button#btn-subscribe:hover {
    background-color: #2844aa;
    color: white;
  }
  div#socials a {
    color: white;
  }
  div#socials a:hover {
    color: #2f55d4;
  }
}
</style>
