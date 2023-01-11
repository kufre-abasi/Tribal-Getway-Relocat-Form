<script>
import AppBanner from "@/components/shared/AppBanner";
// import ProjectsGrid from '../components/projects/ProjectsGrid.vue';
// import Button from '../components/reusable/Button.vue';

export default {
  name: "Home",
  components: {
    AppBanner,
    // ProjectsGrid,
    // Button,
  },
  data() {
    return {
      containerClasses: ["bg-image"],
    };
  },
};
</script>

<template>
  <div class="pt-10 bg-primary">
    <!-- Banner -->
    <AppBanner class="mb-10 sm:mb-20 container" />
  </div>
</template>

<style scoped>
.bg-image {
  background-image: url(../assets/images/bg-lekki.png);
  background-size: cover;
  background-color: rgba(6, 24, 1, 0.863) 18;
  background-blend-mode: overlay;
}
</style>
