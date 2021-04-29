<template>
  <div id="lawn-care" class="overflow-hidden">

    <div class="grid grid-cols-1 gap-4 md:grid-cols-2 ">

      <div class="flex flex-wrap content-between">
        <div class="w-full px-2">
          <h2 class="mb-2 text-4xl font-semibold text-yellow-900 md:text-5xl">LAWN CARE</h2>
          <p>
            A perfect lawn is much more than neatly trimmed green grass; it is a
            matter of pride and privilege to have the best lawn on the block.
            Trust the skilled and knowledgeable professionals at Lawn Plus to
            provide you with unsurpassed lawn care services that will make your
            neighbors green with envy.
          </p>
          <p>
            Are you looking for lawn mowing services for your residential or
            commercial property? We have you covered.
          </p>
          <p>
            You can count on us to mow and trim your lawn to perfection on a 
            weekly/bi-weekly or monthly basis. Our lawn care services include:
          </p>

        </div>
          <ul class="px-2 mb-6">
  
            <CheckListItem v-for="item in serviceList" :key="item.id" :item="item" />
          </ul>
        <div class="w-full ">
          <div class="relative h-80">
            <div class="absolute z-30 flex w-full h-full">
              <div
                class="relative z-30 w-full py-4 mx-6 text-white"
              >
                <h2 class="mb-2 mb-4 text-xl font-semibold shadow-text">We pride ourselves on our ability to make your lawn look its absolute best.</h2>
                <span class="px-4 py-1 text-lg font-bold text-gray-700 shadow-lg bg-blue-50 md:text-xl lg:text-2xl">Call Us  (252) 514-8196</span>
                <!-- <button class="px-2 text-lg font-bold text-gray-700 shadow-lg bg-blue-50 hover:bg-green-200">Contact Us</button> -->
              </div>
            </div>
            <div class="absolute top-0 right-0 block w-full h-full shadow-lg">
              <img
                alt="Contact Us"
                class="object-cover h-full min-w-full "
                src="/img/home/stockvault-chairs145498.jpg"
              />
            </div>
          </div>
        </div>
      </div>

      <div class="flex flex-wrap items-start">
          <img
          class="object-cover w-full mb-4 shadow-lg h-1/3"
          src="/img/home/lawn-care-643555.jpg"
          alt="beautiful lawn in Oriental North Carolina"
        />
       
          <img
        class="object-cover w-full mb-4 shadow-lg h-1/3"
        src="/img/home/lawn_care_1578.jpeg"
        alt="Lush Lawn in Merrit North Carolina"
      />
        
       <div class="overflow-hidden shadow-lg h-1/3">
          <img
          class="object-cover min-h-full"
        src="/img/home/lawn_care_1575_cleanup.jpg"
        alt="Beautiful lawn care results in Arapahoe North Carolina"
      />
       </div>
        
      </div>
    </div>
  </div>
</template>

<script>
  import CheckListItem from "@/components/CheckListItem.vue";
  export default {
    data() {
      return {
        serviceList: [
          {id: 0, text: 'SPRING & FALL CLEANUP'},
          {id: 1, text: 'MOWING -WEEKLY, BI-WEEKLY, MONTHLY'},
          {id: 2, text: 'WEED CONTROL'},
          {id: 3, text: 'GUTTER & ROOFLINE CLEANING'},
          {id: 4, text:  'THATCHING'},
          {id: 5, text:  'BRUSH HOG'},
          {id: 6, text: 'ESTATE CLEAN OUTS'},
        ]
      }
    },
    components: {
      CheckListItem
    }
  }
  </script>





<style scoped>
p {
  margin-bottom: 1em;
}
.vert-top {
  vertical-align: top;
}



</style>