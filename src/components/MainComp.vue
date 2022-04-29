<template>
  <main>
    <AboutSection />
    <KeyFeaturesSection />
    <QuickStartSection />
    <ToolsSection />
    <SubscriptionCardsSection />
  </main>
</template>

<script>
import AboutSection from "./AboutSection.vue";
import KeyFeaturesSection from "./KeyFeaturesSection.vue";
import QuickStartSection from "./QuickStartSection.vue";
import ToolsSection from "./ToolsSection.vue";
import SubscriptionCardsSection from "./SubscriptionCardsSection.vue";

export default {
  name: "MainComp",
  components: {
    AboutSection,
    KeyFeaturesSection,
    QuickStartSection,
    ToolsSection,
    SubscriptionCardsSection,
  },
};
</script>

<style></style>
