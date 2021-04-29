<template>
  <div id="about-lawns-plus" class="px-8 py-12 bg-gray-200">
    <div class="grid grid-cols-1 gap-8 md:grid-cols-2">
      <!-- about text left -->
      <div class="mb-6">
        <h2 class="mb-2 text-4xl font-semibold text-yellow-800 md:text-6xl">
          ABOUT LAWNS PLUS
        </h2>

        <p class="mt-6">
          Lawns Plus is a full-service, year-round land works, landscaping,
           home services and property maintenance company that
          serves residential and commercial properties and projects across
          Pamlico County, North Carolina.
        </p>
        <p class="mt-6">
          Dave Myers and his team of hard working, dedicated employees are known for their attention to detail and unwavering professionalism. Their commitment to prompt, efficient, superior customer service, understanding their clients’ needs, and building solid lasting professional and personal relationships has made Lawns Plus one of the region’s leading land works and property management contractors, and a highly respected member of the Pamlico county community. Every job and every client is our number one priority.
        </p>
        <!-- <h3 class="mt-6 text-lg font-bold">Landscaping & Lawn Care</h3>
        <p class="mb-6">
          We bring over 12 years of lawn care experience to every job we do. 
        </p>
        <h3 class="text-lg font-bold">Home Services</h3>
        <p class="mb-6">
          Our work in the construction field began with a degree in construction
          carpentry from "NAME OF SCHOOL HERE". Since then we've worked on
          projects large an small. We have 25 years of construction experience
        </p> -->
      </div>

      <!-- about text right -->

      <div class="flex flex-wrap justify-center">
        <img
          class="object-cover w-full bg-no-repeat"
          src="/img/home/home-about-dave-tractor.jpg"
          alt="Man on tractor clearing brush"
        />
        <div class="w-5/6 -mt-12 font-medium text-white bg-contact border-lime">
          <div class="px-8 py-12">
            <h3 class="mb-6">
              At Lawns Plus, our level of commitment knows no limit. We back it
              up with our 100% Satisfaction Guarantee.
            </h3>
            <h3 class="mb-6">
              Our goal is to have every Lawns Plus customer love our service and
              enthusiastically refer us to their friends. This requires total
              commitment on our part.
            </h3>
            <div class="px-2 py-2 text-center border-lime">
              CALL (252) 514-8196
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- cloudinary appears to have a lazy load option. See here: -->
    <!--  <img src="https://res.cloudinary.com/css-tricks/image/upload/f_auto,q_auto/v1568814785/photostream-photos/DSC05466_kwlv0n.jpg" alt="A Toyota Previa covered in graffiti" loading="lazy">-->
  </div>
</template>

<style scoped>
.bg-contact {
  background-image: 
  linear-gradient(
      rgba(0, 0, 0, 0.3),
      rgba(0, 0, 0, 0.3)
    ),
    url(/img/home/home-about-commitment.jpg);
  background-repeat: no-repeat;
  background-size: cover;
}

.border-lime {
  border: solid 1px #eeff84;
}
</style>


