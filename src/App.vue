<template>
  <div id="app">
    <router-view />
    <AboutSection />
    <ProjectsSection />
  </div>
</template>

<script>
import AboutSection from '@/components/AboutSection.vue';
import ProjectsSection from '@/components/ProjectsSection.vue';

export default {
  name: '',
  components: {
    AboutSection,
    ProjectsSection,
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

h2 {
  font-family: var(--headline-font);
}
</style>
