<template>
  <div id="app">
    <router-view />
    <AboutSection />
  </div>
</template>

<script>
import AboutSection from '@/components/AboutSection.vue';

export default {
  name: '',
  components: {
    AboutSection,
  },
};
</script>


<style lang="scss">
:root {
  --headline-font: 'Playfair Display', serif;
}
* {
  box-sizing: border-box;
  margin: 0;
  // border: 1px solid red;
}
</style>
