<template>
  <div v-if="visible" class="wrapper">
    <h4 class="title">お題</h4>
    <div class="theme-text">{{ theme }}</div>
  </div>
</template>

<script>
export default {
  props: {
    visible: {
      type: Boolean,
      required: false,
      default: true,
    },
    theme: {
      type: String,
      required: true,
      default: '',
    },
  },
};
</script>

<style scoped>
.wrapper {
  display: flex;
  background-color: #ffdfc1;
  border-radius: 5px;
  padding: 20px;
  margin-bottom: 40px;
  justify-content: center;
}
.title {
  font-size: 16px;
  font-weight: bold;
  margin: 10px;
  border-radius: 5px;
}
.theme-text {
  padding: 10px;
}
.list {
  padding: 5px 0;
  font-size: 14px;
  border-bottom: 1px solid #e7e7f3;

  a:hover {
    color: #331cbf;
  }

  &::before {
    content: '-';
    margin-right: 5px;
    color: #cacae7;
  }

  &.h2 {
    margin-left: 10px;
  }

  &.h3 {
    margin-left: 20px;
  }
}
</style>
