<template>
  <footer class="footer">
    <p class="cr">© enlightenment</p>
  </footer>
</template>

<style scoped>
@media (min-width: 600px) {
  .footer {
    position: relative;
    padding: 30px 40px 20px;
    z-index: 10;
    color: #2b2c30;
    margin-top: 120px;
    background-color: #fff8dd;
  }
  .cr {
    margin-top: 20px;
    text-align: center;
    color: #616269;
    font-size: 14px;
  }
}
@media (max-width: 600px) {
  .footer {
    position: relative;
    padding: 30px 20px;
    z-index: 10;
    color: #2b2c30;
    margin-top: 20px;
  }
  .cr {
    font-size: 12px;
    margin-top: 10px;
    color: #616269;
    text-align: center;
  }
}
</style>
