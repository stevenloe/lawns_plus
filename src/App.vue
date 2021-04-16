<template>
  <main>
    <PageHeader />
    <!-- <header class="bg-green-400 shadow" v-if="$route.meta.title">
      <div class="max-w-7xl mx-auto py-6 px-4 sm:px-6 lg:px-8"></div>
      <h1 class="text-3xl font-bold leading-tight text-gray-900">
        {{ $route.meta.title }}
      </h1>
    </header> -->

    <router-view />
  </main>
</template>

<script>
import PageHeader from "./components/PageHeader.vue";

export default {
  components: {
    PageHeader,
  },
};
</script>

<style >
.brand-green-alpha {
  background: rgba(72, 134, 11, 0.9);
}
.brand-green {
  background: rgba(72, 134, 11, 1);
}

.brand-green-text {
  color: rgba(72, 134, 11, 1);
}

.shadow-text {
  text-shadow: 1px 1px 2px #333;
}
.check {
  margin: 0.3em 0 0 0;
  padding: 0px 0 1px 35px;
  list-style: none;
  background-image: url(/img/global/check-slim.svg);
  background-repeat: no-repeat;
  background-position: left center;
  background-size: 26px;
}
</style>
