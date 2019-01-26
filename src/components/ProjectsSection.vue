<template>
  <div class="projects-contain">
    <div class="proj-content">
      <h2>Our Projects</h2>
      <div class="project">
      </div>
    </div> <!-- Projects Content End -->
  </div> <!-- Projects Container End -->
</template>

<script>

export default {
  name: 'projects',
  // data() {
  //   proj: [
  //     {
  //       id: 1,
  //       title: 'Arizona Retreat',
  //       img_url: 'proj-img/plc-hld-img/az-ret.jpg',
  //     },
  //     {
  //       id: 2,
  //       title: 'Chelsea Loft',
  //       img_url: 'proj-img/plc-hld-img/ch-loft.jpg',
  //     },
  //     {
  //       id: 3,
  //       title: 'Coastal Connecticut',
  //       img_url: 'proj-img/plc-hld-img/cost-ct.jpg',
  //     },
  //     {
  //       id: 4,
  //       title: 'Greenwich Village Pied a Terre',
  //       img_url: 'proj-img/plc-hld-img/gv-pdt.jpg',
  //     },
  //   ],
  // }
};
</script>

<style lang="scss" scoped>
.projects-contain {
  width: 100vw;
  display: grid;
  grid-template-columns: 1fr 5fr 1fr;
  grid-template-areas:
    ".  content   .";
  .proj-content {
    grid-area: content;
  }
}
</style>
