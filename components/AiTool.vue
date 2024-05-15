<template>
  <div class="mt-16 mb-10">
    <h1 class="mt-4 mb-6 font-bold text-gray-600">{{ category }}</h1>
    <div class="grid grid-cols-2 mg:grid-cols-2 lg:grid-cols-4 gap-6">
      <div
        class="border rounded-md shadow-sm hover:bg-gray-50 transition duration-300"
        v-for="(item, i) in tool"
        :key="i"
      >
        <a :href="item.url" target="_blank" class="block w-full h-full p-4">
          <img
            :src="'/downloads/' + item.image"
            :alt="item.name"
            style="
              width: 50px;
              min-height: 50px;
              border-radius: 10px;
              margin: 0 auto;
            "
          />
          <p class="mt-4 text-gray-500 dark:text-gray-500 text-center text-sm">
            {{ item.name }}
          </p>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    tool: {
      type: Object,
      required: true,
    },
    category: {
      type: String,
      required: true,
    },
  },
  computed: {
    imagePath(img) {
      return "/downloads/" + img;
    },
  },
};
</script>
