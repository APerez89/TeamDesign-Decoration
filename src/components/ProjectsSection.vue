<template>
  <div class="projects-contain">
    <div class="proj-content">
      <h2>Our Projects</h2>

      <div v-for="(project, idx) in data" :key="idx">
        <div
          @click="projectClick(project.id)"
          :class="['item', `h${randomNumber(4)} v${randomNumber(4)}`]"
        >
          <img :src="`img/proj-img/plc-hld-img/${project.cover}`">
          <div class="item__overlay">
            <button>View →</button>
          </div>
        </div>
      </div>

      <div class="project"></div>
    </div>
    <!-- Projects Content End -->
  </div>
  <!-- Projects Container End -->
</template>

<script>
import * as data from '../data.json';

export default {
  name: 'projects',
  data() {
    return {
      data: data.default,
      picked: [],
    };
  },
  methods: {
    randomNumber(limit) {
      return Math.floor(Math.random() * limit) + 1;
    },
    projectClick(route) {
      this.$router.push(route);
    },
  },
};
</script>

<style lang="scss" scoped>
img {
  cursor: pointer;
}

.projects-contain {
  width: 100vw;
  display: grid;
  grid-template-columns: 1fr 5fr 1fr;
  grid-template-areas: '.  content   .';
  .proj-content {
    grid-area: content;
  }
}
</style>
