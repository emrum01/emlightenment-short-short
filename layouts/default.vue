<template>
  <div>
    <nuxt class="background" />
  </div>
</template>

<script>
export default {
  head: {
    bodyAttrs: {
      class: 'background',
    },
  },
};
</script>
<style>
@import '@/assets/styles/reset.css';
.background {
  background-color: #fff8dd;
  height: 100vh;
}
</style>
