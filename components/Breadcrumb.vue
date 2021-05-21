<template>
  <ul class="breadcrumb">
    <li class="breadcrumbList">
      <nuxt-link to="/">記事一覧</nuxt-link>
    </li>
    <li v-if="hasCategory(category)" class="breadcrumbList">
      <nuxt-link :to="`/category/${category.id}/page/1`">{{
        category.name
      }}</nuxt-link>
    </li>
  </ul>
</template>

<script>
export default {
  props: {
    category: {
      type: Object,
      required: false,
      default: () => ({}),
    },
  },
  methods: {
    hasCategory(category) {
      return Object.keys(category).length > 0;
    },
  },
};
</script>

<style lang="scss" scoped>
@import '@/assets/scss/_variable.scss';
.breadcrumb {
  display: flex;
  flex-wrap: wrap;
  padding-top: 20px;
}

.breadcrumbList {
  color: $color-secondary-base;

  a {
    color: $color-secondary-base;
  }

  &::after {
    content: '>';
    margin: 0 10px;
  }

  &:last-child &::after {
    content: '';
    margin: 0;
  }
}
@media (max-width: 600px) {
  .breadcrumbList {
    font-size: 14px;
  }
}
</style>
