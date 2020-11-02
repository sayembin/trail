<template>
  <burger
    :nav-links="navLinks"
    :image-path="require('./assets/logo.png')"
    background="#fff"
  ></burger>
  <MainImage />
  <Slide />
</template>
<script>
import Burger from "@/components/Burger.vue";
import MainImage from "@/components/MainImage.vue";
import Slide from "@/components/Slide.vue";

export default {
  name: "App",
  components: {
    Burger,
    MainImage,
    Slide,
  },
  data: () => ({
    navLinks: [
      {
        text: "Gratis Testpaket",
        path: "/",
        icon: "",
      },
      {
        text: "Flexibles Abo",
        path: "/about",
        icon: "",
      },
      {
        text: "Magazin",
        path: "/",
        icon: "ion-ios-bonfire",
      },
      {
        text: "Über LILLYDOO",
        path: "/",
        icon: "",
      },
    ],
  }),
};
</script>

<style lang="scss">
figure {
  margin-block-start: 0;
  margin-block-end: 0;
  margin-inline-start: 10px;
  margin-inline-end: 0;
}
body {
  margin: 0;
}
#app {
  font-family: Roboto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
