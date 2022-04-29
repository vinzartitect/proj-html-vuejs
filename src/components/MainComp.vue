<template>
  <main>
    <AboutSection />
    <KeyFeaturesSection />
    <QuickStartSection />
  </main>
</template>

<script>
import AboutSection from "./AboutSection.vue";
import KeyFeaturesSection from "./KeyFeaturesSection.vue";
import QuickStartSection from "./QuickStartSection.vue";

export default {
  name: "MainComp",
  components: {
    AboutSection,
    KeyFeaturesSection,
    QuickStartSection,
  },
};
</script>

<style></style>
