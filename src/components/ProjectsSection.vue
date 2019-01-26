<template>
  <div class="projects-contain">
    <div class="proj-content">
      <h2>Our Projects</h2>
      <div class="projects">
      </div>
    </div> <!-- Projects Content End -->
  </div> <!-- Projects Container End -->
</template>

<script>

export default {
  name: 'projects',
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
