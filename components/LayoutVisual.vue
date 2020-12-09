<template>
  <div
    class="relative pt-10 pb-32 flex content-center items-center justify-center z-10 opacity-75"
    :style="`min-height: ${height}vh;`"
  >
    <div
      :class="`absolute top-0 w-full h-full bg-center bg-cover ${visual}`"
    ></div>
    <div class="container relative mx-auto">
      <div class="items-center">
        <div class="w-full px-4 mx-auto text-center">
          <h1 class="text-white font-semibold text-5xl title">
            {{ title }}
          </h1>
          <p v-if="message" class="text-white font-medium text-lg title">
            {{ message }}
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'LayoutVisual',
  props: {
    title: {
      type: String,
      default: '',
    },
    message: {
      type: String,
      default: '',
    },
    visual: {
      type: String,
      default: 'visual-home',
    },
    height: {
      type: Number,
      default: 53,
    },
  },
}
</script>

<style>
.visual-home {
  background-image: url('../assets/img/visual-home.jpg');
}
.visual-concept {
  background-image: url('../assets/img/visual-concept.png');
}
.visual-shop {
  background-image: url('../assets/img/visual-shop.png');
}
.visual-menu {
  background-image: url('../assets/img/visual-menu.png');
}
.visual-information {
  background-image: url('../assets/img/visual-information.png');
}
.visual-error {
  background-image: url('../assets/img/visual-home.jpg');
}
.title {
  text-shadow: 0px 5px 3px darkgray;
}
</style>
