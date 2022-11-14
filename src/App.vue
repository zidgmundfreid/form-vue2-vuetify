<template>
  <v-app class="wrapper">
    <HeaderComponent />
    <FormComponent />
    <FooterComponent />
  </v-app>
</template>

<script>
import FormComponent from './components/FormComponent';
import HeaderComponent from './components/HeaderComponent';
import FooterComponent from './components/FooterComponent';

export default {
  name: 'App',

  components: {
    FormComponent,
    HeaderComponent,
    FooterComponent,
  },
  data: () => ({

  }),
};
</script>

<style>
.v-application--wrap {
  height: 100%;
  background-image: url(./assets/bg-coverbackground.jpg);
  background-size: 100%;

}

</style>
