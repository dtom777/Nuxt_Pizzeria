<template>
  <div :class="`${classPosition} ${classMargin} mb-5 mx-auto`">
    <a
      :href="link"
      :class="`bg-white shadow-xl px-4 py-4 hover:bg-opacity-50 ${classShape} ${classBackGroundColor} ${classBackGroundHoverColor} ${classTextColor} text-lg font-semibolds`"
      >{{ name }}</a
    >
  </div>
</template>

<script>
export default {
  name: 'BaseButton',
  props: {
    name: {
      type: String,
      required: true,
    },
    link: {
      type: String,
      required: true,
    },
    classPosition: {
      type: String,
      default: 'text-center',
    },
    classMargin: {
      type: String,
      default: '',
    },
    classShape: {
      type: String,
      default: 'rounded-xl',
    },
    classBackGroundColor: {
      type: String,
      default: 'bg-white',
    },
    classBackGroundHoverColor: {
      type: String,
      default: 'hover:bg-opacity-50',
    },
    classTextColor: {
      type: String,
      default: 'text-gray-900',
    },
  },
}
</script>
