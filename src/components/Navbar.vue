<template>
  <header class="block py-4 brand-green-alpha md:p-0">
    <div class="flex justify-between">
      <Logo class="self-center mx-6 "/>
      <!-- <Logo class="self-center mx-6 sm:bg-blue-300 md:bg-yellow-300 lg:bg-red-300 xl:bg-green-300 2xl:bg-indigo-900"/> -->

      <div class="self-center hidden px-6 py-4 text-white bg-green-800 md:block rounded-bl-xl ">
        <p class="font-bold">(252) 514-8196</p>
        <p>Oriental, NC</p>
      </div>

      <!--  menu open / close -->
      <div class="self-center mx-6 md:hidden">
        <button
          @click="isOpen = !isOpen"
          type="button"
          class="block text-white hover:text-white focus:text-white focus:outline-none"
        >
          <svg class="w-6 h-6 fill-current" viewBox="0 0 24 24">
            <path
              v-if="isOpen"
              fill-rule="evenodd"
              d="M18.278 16.864a1 1 0 0 1-1.414 1.414l-4.829-4.828-4.828 4.828a1 1 0 0 1-1.414-1.414l4.828-4.829-4.828-4.828a1 1 0 0 1 1.414-1.414l4.829 4.828 4.828-4.828a1 1 0 1 1 1.414 1.414l-4.828 4.829 4.828 4.828z"
            />
            <path
              v-if="!isOpen"
              fill-rule="evenodd"
              d="M4 5h16a1 1 0 0 1 0 2H4a1 1 0 1 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2z"
            />
          </svg>
        </button>
      </div>
    </div>
    <div class="relative">
      <nav
        :class="isOpen ? 'block ' : 'hidden'"
        class="absolute justify-between w-full px-4 py-6 mt-4 md:py-0 md:flex brand-green-alpha md:mt-0"
      >
        <NavItem v-for="item in navItems" :key="item.id" :item="item" @click="onNavClick" />
      </nav>
    </div>
  </header>
</template>

<script>
import Logo from "./Logo.vue";
import NavItem from "./NavItem.vue";
export default {
  data() {
    return {
      isOpen: false,
      navItems: [
        { id: 0, text: "Lawn Care", url: "#lawn-care" },
        { id: 1, text: "Home Services", url: "#home-services" },
        { id: 2, text: "Landcaping", url: "#landscaping" },
        { id: 3, text: "Spring & Fall Cleanup", url: "#spring-and-fall-cleanup" },
        { id: 4, text: "Power Washing", url: "#power-washing" },
        { id: 5, text: "About", url: "#about-lawns-plus" },
        // { id: 6, text: "Contact", url: "#" },
      ],
    };
  },
  components: { Logo, NavItem },
  methods: {
    onNavClick() {
      console.log(" ON navclick");
      this.isOpen = false
    }
  }
};
</script>