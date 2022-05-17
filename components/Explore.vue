<template>
  <div class="p-10">
    <p v-if="$fetchState.pending">Loading....</p>
    <p v-else-if="$fetchState.error">Error while fetching mountains</p>
    <ul v-else class="grid grid-cols-3 gap-3">
      <li
        class="rounded shadow-lg bg-gray-200"
        v-for="(mountain, index) in mountains"
        :key="index"
      >
        <img class="object-cover h-48 w-96" :src="mountain.image" />
        <div class="px-6 py-4">
          <div class="font-bold text-xl mb-2">{{ mountain.title }}</div>
          <div class="text-gray-700 text-sm">{{ mountain.description }}</div>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      mountains: [],
    };
  },
  async fetch() {
    this.mountains = await fetch("https://api.nuxtjs.dev/mountains").then(
      (res) => res.json()
    );
  },
};
</script>