<template>
  <div id="home-services" class="w-full mb-4 wood-bg">
    <div
      class="w-full h-full grid-cols-2 grid-rows-1 gap-8 p-6 md:p-12 md:grid"
    >
      <!--  white box left -->
      <div class="col-span-1 row-span-1 p-3 bg-white md:p-6">
        <!-- image grid screens 767 px wide and below -->
        <div v-if="isMobile" class="h-full">
          <img loading="lazy"
            alt="Carpenter building custom shelves"
            class="object-cover w-full h-48 sm:h-56"
            src="/img/home/home-services-4_h200.jpg"
            srcset="/img/home/home-services-4_h200.jpg 1x,
              /img/home/home-services-4_h400.jpg 2x,
              /img/home/home-services-4_h800.jpg 3x"
          />
        </div>

        <!-- image grid screen 768px wide and above-->
        <div v-else class="grid h-full grid-cols-12 gap-2 grid-rows-12">
          <!-- row 1 -->
          <div class="col-span-12 overflow-hidden bg-yellow-800 row-span-7">
            <img loading="lazy"
              alt="Carpenter building custom shelves"
              class="object-cover min-h-full"
              src="/img/home/home-services-1_1x.jpg"
              srcset="/img/home/home-services-1_1x.jpg 1x,
              /img/home/home-services-1_2x.jpg 2x,
              /img/home/home-services-1_3x.jpg 3x"
            />
          </div>

          <!-- row 2 -->
          <div class="col-span-8 row-span-2 overflow-hidden bg-yellow-800 ">
            <img loading="lazy"
              alt="Carpenter building custom shelves"
              class="object-cover min-w-full min-h-full"
              src="/img/home/home-services-2_1x.jpg"
              srcset="/img/home/home-services-2_1x.jpg 1x,
              /img/home/home-services-2_2x.jpg 2x,
              /img/home/home-services-2_3x.jpg 3x"
            />
          </div>

          <div class="col-span-4 row-span-2 overflow-hidden bg-yellow-700 ">
            <img loading="lazy"
              alt="Carpenter building custom shelves"
              class="object-cover min-w-full min-h-full"
              src="/img/home/home-services-3_1x.jpg"
              srcset="/img/home/home-services-3_1x.jpg 1x,
              /img/home/home-services-3_2x.jpg 2x,
              /img/home/home-services-3_3x.jpg 3x"
            />
          </div>

          <!-- row 3 -->
          <div class="col-span-6 row-span-3 overflow-hidden bg-yellow-800 ">
            <img loading="lazy"
              alt="Carpenter building custom shelves"
              class="object-cover min-w-full min-h-full"
              src="/img/home/home-services-4_h200.jpg"
              srcset="/img/home/home-services-4_h200.jpg 1x,
              /img/home/home-services-4_h400.jpg 2x,
              /img/home/home-services-4_h800.jpg 3x"
            />
          </div>
          <div class="col-span-6 row-span-3 overflow-hidden bg-yellow-700 ">
            <img loading="lazy"
              alt="Carpenter building custom shelves"
              class="object-cover min-w-full min-h-full"
              src="/img/home/home-services-5_h200.jpg"
              srcset="/img/home/home-services-5_h200.jpg 1x,
              /img/home/home-services-5_h400.jpg 2x,
              /img/home/home-services-5_h800.jpg 3x"
            />
          </div>
        </div>
      </div>

      <!-- white box right -->
      <div class="col-span-1 p-6 pt-0 bg-white md:h-full md:pt-6">
        <h1
          class="mb-2 text-3xl font-semibold text-yellow-900 md:text-4xl lg:text-5xl"
        >
          HOME SERVICES
        </h1>
        <p class="mb-4 font-">
          With 25 years of residential construction & facilities management
          experience, we have what it takes to handle your project.
        </p>
        <p class="mb-4">
          Recent jobs include: building an area divider wall for a homeowner in
          Merrit, adding a deck to a home in Arapahoe, creating a custom
          built-in desk for a business in Oriental, and replacing a hot water
          heater for a business in Bayboro.
        </p>

        <ul>
          <CheckListItem
            v-for="item in serviceList"
            :key="item.id"
            :item="item"
          />
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
import { debounce } from "@/utils/debounce.js";
import CheckListItem from "@/components/CheckListItem.vue";
export default {
  data() {
    return {
      isMobile: true,
      serviceList: [
        { id: 0, text: "LIGHT CARPENTRY" },
        { id: 1, text: "PLUMBING" },
        { id: 2, text: "TILE" },
        { id: 3, text: "GUTTER & ROOFLINE CLEANING" },
        { id: 4, text: "ESTATE CLEAN OUTS" },
      ],
    };
  },
  mounted: function () {
    this.onResize();
    window.addEventListener("resize", debounce(this.onResize, 35));
  },
  methods: {
    onResize() {
      this.isMobile = this.isSearchOpen = window.innerWidth < 767;
      console.log("----- NAVBAR RESIZE----", this.isMobile);
      // this.$bus.$emit("resize-window");
    },
  },
  components: {
    CheckListItem,
  },
};
</script>


<style scoped>
h3 {
  color: rgb(175, 211, 34);
}
.wood-bg {
  background: url(/img/home/bg-home-services_500.jpg);
}
@media (min-width: 768px) {
  .wood-bg {
    background: url(/img/home/bg-home-services_1000.jpg);
  }
}
</style>

