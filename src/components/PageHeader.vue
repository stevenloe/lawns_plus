<template>
  <div class="aspect-w-16 aspect-h-14">
    <div class="hero-image">
      <Navbar />

      <div class="flex flex-wrap h-full md:pt-36">
        <div class="flex justify-between w-full px-6 md:hidden">

        <p class="font-semibold text-white shadow-text">Oriental, NC</p>
        <p class="font-extrabold text-white shadow-text">Call (252) 514-8196</p>
        </div>

        <div
          class="px-12 -mt-12 text-3xl text-center text-white sm:text-5xl md:text-7xl md:mt-36 lg:text-8xl lg:mt-64 2xl:text-9xl 2xl:mt-96"
        >
          OUR LEVEL OF COMMITMENT KNOWS 
          <span class="font-extrabold">NO LIMIT</span>
        </div>

        <div class="w-full -mt-16 text-center">
          <div class="text-base text-xl font-semibold text-center text-white md:text-4xl">
            Prouldy Serving Pamlico County
          </div>
          <div class="text-base text-center text-white md:text-4xl">
            Licensed & Insured
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Navbar from "./Navbar.vue";
export default {
  data() {
    return {
      isOpen: false,
    };
  },
  components: {
    Navbar,
  },
};
</script>


<style scoped>


.hero-image {
  background: url("/img/hero/bg-home-hero_1000.jpg");
  background-repeat: no-repeat;
  background-size: cover;
}


@media (min-width: 950px) {
    .hero-image {
      background: url("/img/hero/bg-home-hero_1440.jpg");
      background-repeat: no-repeat;
      background-size: cover;
    }
}
</style>