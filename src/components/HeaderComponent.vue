<template>
  <div class="header-container">
    <img style="cursor: pointer" width="198" height="48" :src="logo" />
    <h1>
      <a href="#" style="font-weight: bold; cursor: pointer">Sign Up</a> and find the best place to
      rest while traveling
    </h1>
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
.header-container {
  padding-top: 120px;
  text-align: center;
  padding-bottom: 55px;
}

h1 {
  padding-top: 30px;
  color: #ffffff;
  font-weight: 500;
  font-size: 24px;
  line-height: 28px;
  text-align: center;
}
a {
  text-decoration: none;
  color: #6ceec7 !important;
  font-weight: 500;
  font-size: 24px;
  line-height: 28px;
  text-align: center;
}
</style>
