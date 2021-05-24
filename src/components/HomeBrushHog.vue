<template>
  <div class="mb-4 bg-image aspect-w-4 aspect-h-3 ">
    <div class="flex flex-wrap">
      <h1 id="spring-and-fall-cleanup"
        class="mt-8 ml-8 text-4xl font-semibold text-white shadow-text md:text-6xl"
      >
        BRUSH HOG
      </h1>
      <div class="flex justify-end w-full mb-2 md:justify-start md:mb-12">
        <div
        class="self-end w-3/4 p-4 pr-4 font-medium text-white rounded lg:p-8 lg:text-xl lg:leading-8 transparent-box md:w-1/3 md:self-start lg:rounded-3xl"
        >
          Let us quickly cut and clear the overgrown brush on your property.
        </div>
      </div>
    </div>
  </div>
</template>


<style scoped>
.bg-image {
  background: url("/img/home/home-brush-hog-vignette_500.jpg");
  background-repeat: no-repeat;
  background-size: cover;
}

@media (min-width: 760px) {
    .bg-image {
      background: url("/img/home/home-brush-hog-vignette_1000.jpg");
    }
}
@media (min-width: 950px) {
    .bg-image {
      background: url("/img/home/home-brush-hog-vignette_1500.jpg");
    }
}

.transparent-box {
  background: rgba(40, 81, 2, 0.80);
}
</style>