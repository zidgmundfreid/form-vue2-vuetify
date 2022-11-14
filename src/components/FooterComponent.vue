<template>
  <div class="footer-container">
    <p>
      If you have an account,
      <a href="#" style="font-weight: bold; cursor: pointer; font-weight: bold">Log In</a>
    </p>
  </div>
</template>

<script>
export default {
  data: () => ({
    logo: require('../assets/logo.svg'),
  }),
};
</script>

<style scoped>
.footer-container {
  padding-top: 80px;
  padding-bottom: 40px;
}
p {
  padding-top: 30px;
  color: #ffffff;
  font-weight: 300;
  font-size: 15px;
  line-height: 18px;
  text-align: center;
}

p > a {
  color: #6ceec7;
  font-weight: 300;
  font-size: 15px;
  line-height: 18px;
  text-align: center;
}
</style>
