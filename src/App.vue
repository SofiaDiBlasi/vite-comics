<script>
  import AppHeaderVue from './components/AppHeader.vue';
  import AppMainVue from './components/AppMain.vue';
  import AppFooter from './components/AppFooter.vue';

  export default {
    name: 'App',
      components: {
        AppHeaderVue,
        AppMainVue,
        AppFooter
      }
  }
</script>

<template>
  <AppHeaderVue />
  <AppMainVue />
  <AppFooter />
</template>

