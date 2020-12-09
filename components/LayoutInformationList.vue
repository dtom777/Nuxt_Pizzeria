<template>
  <div class="mb-5">
    <div class="mb-4 mx-4">
      <div class="bg-blue-100 border-t-4 border-blue-400 shadow-md">
        <a :href="'/information/' + id + '/'" class="block px-4 py-3">
          <time class="block text-gray-600 mb-1">{{ date | formatDate }}</time>
          <div>{{ title }}</div>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'LayoutInformation',
  props: {
    title: {
      type: String,
      required: true,
    },
    date: {
      type: String,
      required: true,
    },
    id: {
      type: String,
      required: true,
    },
  },
}
</script>
