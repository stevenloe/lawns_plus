<script>
import { defineComponent } from "vue";
import HomeLawnCare from "@/components/HomeLawnCare.vue";
import HomeLandscaping from "@/components/HomeLandscaping.vue";
import HomeServices from "@/components/HomeServices.vue";
import Cleanup from "@/components/Cleanup.vue";
import HomePowerWashing from "@/components/HomePowerWashing.vue";
import HomeAbout from "@/components/HomeAbout.vue";
import Footer from "@/components/Footer.vue";

export default defineComponent({
  components: {
    HomeLawnCare,
    HomeLandscaping,
    HomeServices,
    Cleanup,
    HomePowerWashing,
    HomeAbout,
    Footer,
  },
});
</script>

<template>
  <main>
    <div class="bg-gray-50">
      <div
        class="max-w-screen-xl px-4 py-12 mx-auto sm:px-6 lg:py-16 lg:px-8 lg:items-center lg:justify-between"
      >
        <HomeLawnCare />
        <HomeLandscaping />
        <HomeServices/>
        <Cleanup class="mb-8"/>
        <HomePowerWashing />
        <HomeAbout />
      </div>
        <Footer />
    </div>
  </main>
</template>