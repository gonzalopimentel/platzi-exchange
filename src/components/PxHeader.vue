<template>
  <header class="shadow w-screen">
    <nav class="flex items-center justify-between flex-wrap bg-green-400 p-6">
      <div class="flex items-center flex-shrink-0 text-white mr-6">
        <px-icon class="mr-2" />
        <router-link
          :to="{ name: 'home' }"
          class="font-semibold text-xl tracking-tight hover:text-red-700"
          >ZaloExchange</router-link
        >
      </div>
      <div
        class="hidden sm:hidden w-full flex-grow lg:flex lg:items-center lg:w-auto"
      >
        <div class="text-sm lg:flex-grow">
          <router-link
            v-for="l in links"
            :key="l.title"
            :to="l.to"
            class="block mt-4 lg:inline-block lg:mt-0 text-teal-200 hover:text-white mr-4"
            >{{ l.title }}</router-link
          >
        </div>
      </div>
      <div class="mr-10">
        <router-link
          class="font-semibold text-xl text-white tracking-tight hover:text-red-700"
          :to="{ name: 'about' }"
          >About</router-link
        >
      </div>
      <div>
        <router-link
          class="font-semibold text-xl text-white tracking-tight hover:text-red-700"
          :to="{ name: 'error' }"
          >Do not touch</router-link
        >
      </div>
    </nav>
  </header>
</template>

<script>
import PxIcon from "@/components/PxIcon";
export default {
  name: "PxHeader",
  components: { PxIcon },
  props: {
    links: {
      type: Array,
      default: () => []
    }
  }
};
</script>
