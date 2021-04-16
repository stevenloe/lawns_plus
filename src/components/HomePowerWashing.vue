<template>
  <div class="mb-2">
    <div class="bg-image sm:aspect-w-4 aspect-h-4 sm:aspect-h-5 md:aspect-h-3">
      <div class="flex flex-wrap">
        <h2
          class="mt-8 mb-2 ml-8 text-4xl font-semibold text-white shadow-text md:text-6xl"
        >
          POWER WASHING
        </h2>
        <div class="flex justify-start w-full h-full mt-6 md:justify-end">
          <div
            class="self-start w-3/4 p-4 pr-4 mb-1 font-medium text-white lg:p-8 lg:text-xl lg:leading-8 transparent-box md:w-1/2 lg:w-1/3 lg:rounded-3xl"
          >
            We can make your home or business clean & crisp by removing the
            mold, mildew, algae, and dirt that time and the moist North Carolina
            climate have left behind.
          </div>
        </div>
      </div>
    </div>
    <ul>
  <li>
    <img src="/img/home/power-washing1.jpg" alt="Power washing a walkway in Arapahoe, North Carolina" loading="lazy">
  </li>
  <li class="hidden lg:block">
    <img src="/img/home/power-washing2.jpg" alt="A clean power washed sailboat" loading="lazy">
  </li>
  <li>
    <img src="/img/home/power-washing3.jpg" alt="Man power washing a boat" loading="lazy">
  </li>
  <li class="hidden sm:block">
    <img src="/img/home/power-washing4.jpg" alt="A freshly power washed shed in Oriental North Carolina" loading="lazy">
  </li>
  <li class="hidden sm:block">
    <img src="/img/home/power-washing5.jpg" alt="Clean power washed Airstream travel trailer" loading="lazy">
  </li>
  <li class="hidden lg:block">
    <img src="/img/home/power-washing6.jpg" alt="Clean power washed boat in Merritt, NC" loading="lazy">
  </li>
</ul>

<!-- cloudinary appears to have a lazy load option. See here: -->
<!--  <img src="https://res.cloudinary.com/css-tricks/image/upload/f_auto,q_auto/v1568814785/photostream-photos/DSC05466_kwlv0n.jpg" alt="A Toyota Previa covered in graffiti" loading="lazy">-->
    
  </div>
</template>


<style scoped>
.bg-image {
  background: url("/img/home/powerwash1-istockphoto-184370884-1024x1024.jpg");
  background-repeat: no-repeat;
  background-size: cover;
}
.transparent-box {
  background: rgba(40, 81, 2, 0.66);
}

/* row of images at bottom */

ul {
  display: flex;
  flex-wrap: no-wrap;
  justify-content: space-between;
}

li {
  flex-grow: 1;
 
}

li:not(:first-child) {
    margin-left: 0.3rem;
}



img {
  max-height: 100%;
  min-width: 100%;
  object-fit: cover;
  vertical-align: bottom;
}
</style>