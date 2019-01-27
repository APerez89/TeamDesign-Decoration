<template>
  <div class="projects-contain">
    <div class="proj-content">
      <h2>Our Projects</h2>

      <div v-for="(project, idx) in data.default" :key="idx">
        <div class="item h${randomNumber(4)} v${randomNumber(4)}" @click="projectClick()">
          <img :src="`img/proj-img/plc-hld-img/${chooseImage()}.jpg`">
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
import * as data from "../data.json";

export default {
  name: "projects",
  data() {
    return {
      data,
      picked: []
    };
  },
  methods: {
    randomNumber(limit) {
      return Math.floor(Math.random() * limit) + 1;
    },
    chooseImage() {
      const a = this.randomNumber(4);
      // if (this.picked.includes(a)) {
      //   a = this.randomNumber(4);
      // }

      this.picked.push(a);
      console.log("herro");
    },
    projectClick(route) {
      // $route.push(route);
    }
  }
};
</script>

<style lang="scss" scoped>
.projects-contain {
  width: 100vw;
  display: grid;
  grid-template-columns: 1fr 5fr 1fr;
  grid-template-areas: ".  content   .";
  .proj-content {
    grid-area: content;
  }
}
</style>
