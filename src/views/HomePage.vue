<template>
  <div class="home-contain">
    <div class="hm-content">
      <h1>Team Design and <br>Decoration</h1>
      <div class="nav-1">
        <a href="#">Contact</a>
        <a href="#">Instagram</a>
      </div> <!-- Nav-1 End -->
      <div class="nav-2">
        <ul>
          <li class="circle"> <a href="#"></a> </li>
          <li class="circle"> <a href="#"></a> </li>
          <li class="circle"> <a href="#"></a> </li>
        </ul>
      </div> <!-- Nav-2 End -->
      <div class="arrow"><i id="arrow" class="fas fa-chevron-circle-down"></i></div>
    </div> <!-- HM Content End -->
    <div class="contact">
      <div class="contact-info">
        <p>EMAIL: RICK@TEAMDESIGNANDDECORATION.COM</p>
        <P>PHONE: (917)292-7700</P>
      </div>
    </div>
  </div> <!-- Home Contain End -->
</template>

<script>

export default {
  name: 'home',
};
</script>

<style lang="scss" scoped>
.home-contain {
  display: grid;
  width: 100vw;
  height: 100vh;
  background-image: url('/img/cover/cover-img.jpg');
  background-size: cover;
  background-repeat: no-repeat;
  background-position: 50%;
  .hm-content {
    display: grid;
    grid-template-columns: 1fr 5fr 1fr;
    grid-template-rows: 50px repeat(3, 1fr);
    grid-template-areas:
      ".        .         nav-1"
      "headline headline  headline"
      ".        .         nav-2"
      "footer   footer    footer";
    margin: 30px;
    h1 {
      font-family: var(--headline-font);
      font-variant: small-caps;
      font-size: 60px;
      font-weight: 100;
      letter-spacing: 5px;
      text-align: center;
      color: #fff;
      text-shadow: 0px 2px 13px rgba(0, 0, 0, 0.3);
      grid-area: headline;
    }
    .nav-1 {
      grid-area: nav-1;
      padding: 10px 0;
      a {
        font-family: var(--headline-font);
        text-decoration: none;
        letter-spacing: 5px;
        padding: 10px 25px;
        color: #fff;
        &:hover {
          color: red;
        }
      }
    }
    .nav-2 {
      grid-area: nav-2;
      display: grid;
      align-content: center;
      ul {
        display: grid;
        justify-content: end;
        padding: 0;
        list-style: none;
        .circle {
          border: 1.5px solid #fff;
          border-radius: 50px;
          margin: 10px;
          padding: 5px;
        }
      }
    }
    @mixin keyframes($name) {
      @keyframes #{$name} {
        @content;
      }
    }
    @mixin animation($value) {
      animation: $value;
    }
    @include keyframes(move) {
      0% { bottom: 0; }
      100% { bottom: 5px; }
    }
    .arrow {
      display: grid;
      justify-content: center;
      align-items: end;
      grid-area: footer;
      font-size: 50px;
      color: rgba(255, 255, 255, 0.5);
      #arrow {
        position: relative;
        @include animation(move 0.6s ease-in-out infinite alternate);
      }
    }
  }
}
</style>
