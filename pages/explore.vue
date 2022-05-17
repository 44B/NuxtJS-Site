<template>
  <div>
    <ul class="flex border-b flex justify-center">
      <li class="mr-1">
        <NuxtLink
          class="
            bg-white
            inline-block
            py-2
            px-4
            text-blue-500
            hover:text-blue-800
            font-semibold
          "
          to="/"
          >Home</NuxtLink
        >
      </li>
      <li class="mr-1">
        <NuxtLink
          class="
            bg-white
            inline-block
            py-2
            px-4
            text-blue-500
            hover:text-blue-800
            font-semibold
          "
          to="/explore"
          >Explore</NuxtLink
        >
      </li>
    </ul>
    <Explore />
  </div>
</template>

<script>
import Vue from "vue";
export default Vue.extend({
  name: "ExplorePage",
});
</script>