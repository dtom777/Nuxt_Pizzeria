<template>
  <div :class="itemClass">
    <div :class="blockClass">
      <img v-if="image" :src="imageUrl" :alt="name" :class="imageClass" />
      <img
        v-else
        src="~/assets/img/dummy.png"
        :alt="name"
        :class="imageClass"
      />
      <div :class="dataClass">
        <div
          class="md:font-bold font-semibold md:text-lg md:mb-5 mb-0 text-center"
        >
          {{ name }}
        </div>
        <p v-if="flagBody" class="mb-2 text-sm md:text-base">{{ body }}</p>
        <p class="md:font-medium mb-2 text-center">{{ price }}円</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'LayoutMenuList',
  props: {
    itemClass: {
      type: String,
      default: 'md:w-full mb-5 shadow-lg mx-auto text-center w-4/5',
    },
    blockClass: {
      type: String,
      default:
        'md:w-full bg-white flex flex-wrap justify-between md:px-2 md:py-2',
    },
    imageClass: {
      type: String,
      default: 'w-full md:w-2/5',
    },
    dataClass: {
      type: String,
      default: 'md:w-7/12 w-full md:leading-relaxed md:pt-5',
    },
    flagBody: {
      type: Boolean,
      default: true,
    },
    image: {
      type: Object,
      required: true,
    },
    imageUrl: {
      type: String,
      required: true,
    },
    name: {
      type: String,
      required: true,
    },
    body: {
      type: String,
      required: true,
    },
    price: {
      type: Number,
      required: true,
    },
  },
}
</script>
