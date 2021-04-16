<template>
  <div class="w-full wood-bg">
    <div
      class="w-full h-full p-6 md:p-12 md:grid grid-cols-2 grid-rows-1 gap-8"
    >
      <!--  white box left -->
      <div class="col-span-1 row-span-1 bg-white p-3 md:p-6">

        <!-- image grid screens 767 px wide and below -->
        <div v-if="isMobile" class="h-full">
            <img
              alt="Carpenter building custom shelves"
              class="object-cover h-48 sm:h-56 w-full"
              src="/img/home/home-services-4.jpg"
            />
        </div>

        <!-- image grid screen 768px wide and above-->
        <div v-else class="grid grid-cols-12 grid-rows-12 gap-2 h-full">
          <!-- row 1 -->
          <div class="col-span-12 row-span-7 bg-indigo-100 overflow-hidden">
            <img
              alt="Carpenter building custom shelves"
              class="object-cover min-h-full"
              src="/img/home/home-services-1.jpg"
            />
          </div>

          <!-- row 2 -->
          <div class="col-span-8 row-span-2 bg-pink-200 overflow-hidden">
            <img
              alt="Carpenter building custom shelves"
              class="object-cover min-w-full min-h-full"
              src="/img/home/home-services-2.jpg"
            />
          </div>

          <div class="col-span-4 row-span-2 bg-pink-300 overflow-hidden">
            <img
              alt="Carpenter building custom shelves"
              class="object-cover min-w-full min-h-full"
              src="/img/home/home-services-3.jpg"
            />
          </div>

          <!-- row 3 -->
          <div class="col-span-6 row-span-3 bg-green-100 overflow-hidden">
            <img
              alt="Carpenter building custom shelves"
              class="object-cover min-w-full min-h-full"
              src="/img/home/home-services-4.jpg"
            />
          </div>
          <div class="col-span-6 row-span-3 bg-green-400 overflow-hidden">
            <img
              alt="Carpenter building custom shelves"
              class="object-cover min-w-full min-h-full"
              src="/img/home/home-services-5.jpg"
            />
          </div>
        </div>
      </div>

      <!-- white box right -->
      <div class="bg-white col-span-1 md:h-full p-6 pt-0 md:pt-6">
        <h1
          class="text-3xl md:text-4xl lg:text-5xl font-semibold text-yellow-900 mb-2"
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
  background: url(/img/home/bg-home-services.jpg);
}
</style>

