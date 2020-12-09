<template>
  <div class="wrapper">
    <slot />
  </div>
</template>

<script>
export default {
  name: 'LayoutWrapper',
}
</script>

<style scoped>
.wrapper {
  padding-top: 80px;
  background-color: rgb(226, 232, 240);
  padding-bottom: 1rem;
  @media (min-width: 768px) {
    padding-top: 0px;
  }
}
</style>
