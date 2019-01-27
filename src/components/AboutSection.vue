<template>
  <div class="about-contain">
    <div class="ab-content">
      <h2>About</h2>
      <!--eslint-disable-->
      <p>Rick Garofalo has been a champion in the design industry in the United States since the late 80’s. Founded in 1988 by Rick, repertoire became one of the premier design ateliers in the United States bringing the worlds best design to Boston and eventually New York. Repertoire created residential and commercial projects of great distinction until 2005. Since 2005, originally based in New York City, reinvented as Team Design and Decoration has worked on projects in New York City, The Hamptons, Westchester County Florida and Arizona. In 2015, having done a project in Rowayton, Connecticut, Rick fell in love with coastal Connecticut and moved the design office to Stamford, an easy commute to service New York City, Westchester and Fairfield Counties. With almost 30 years in the design industry, Rick is known for his creativity, his hands on attention to detail, and sense of humor.</p>
    </div>
    <!-- AB Content End -->
  </div>
  <!-- About Contain End -->
</template>

<script>
export default {
  name: 'about',
};
</script>

<style lang="scss" scoped>
.about-contain {
  width: 100vw;
  height: 700px;
  background-color: #fff;
  display: grid;
  grid-template-columns: 1fr 3fr 1fr;
  grid-template-areas: '.  content   .';
  align-items: center;
  .ab-content {
    display: grid;
    grid-gap: 20px;
    grid-area: content;
    text-align: center;
    h2 {
      font-size: 55px;
      font-weight: 100;
      font-variant: small-caps;
      letter-spacing: 5px;
      color: #8d7e79;
      text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.5);
    }
    p {
      font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen,
        Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
      letter-spacing: 2px;
      font-size: 17px;
      line-height: 50px;
    }
  }
}
</style>
