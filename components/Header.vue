<template>
  <div>
    <header class="header">
      <h1 class="logo">
        enlightenment
      </h1>
    </header>
    <div class="empty"></div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      params: this.params || '',
      open: false,
    };
  },
  mounted() {
    this.params = location.search || '';
  },
};
</script>

<style lang="scss" scoped>
@import '@/assets/scss/_variable.scss';
@media (min-width: 800px) {
  .header {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: center;
    padding: 12px 40px;
    z-index: 10;
    border-bottom: 1px solid var(--color-border);
    background-color: $color-secondary-base;
  }

  .logo {
    display: flex;
    font-family: 'HitchhikerFont';
    justify-content: center;
    color: $color-primary-base;
  }
}

@media (max-width: 800px) {
  .header {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: #3f3934;
    padding: 16px;
    z-index: 10;
    border-bottom: 1px solid var(--color-border);
  }
  .logo {
    font-family: 'HitchhikerFont';
    justify-content: center;
    color: #e68048;
  }
}
</style>
