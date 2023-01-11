<script>
import AppBanner from "@/components/shared/AppBanner";
import ContactForm from "../components/contact/ContactForm.vue";

export default {
  name: "Home",
  components: {
    AppBanner,
    ContactForm,
  },
  data() {
    return {
      containerClasses: ["bg-image"],
    };
  },
};
</script>

<template>
  <div class="">
    <!-- Banner -->
    <AppBanner class="mb-5 sm:mb-8 bg-secondary-dark" />

    <!-- ContactForm -->
    <ContactForm />
  </div>
</template>

<style scoped>
.bg-image {
  background-image: url(../assets/images/bg-lekki.png);
  background-size: cover;
  background-color: rgba(0, 0, 0, 0.418);
  background-blend-mode: overlay;
}
</style>
