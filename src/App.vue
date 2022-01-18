<template>
  <div id="app">
    TEST
    <Header :navItemsArray="navItemsArray" />
    <Main :iconsArray="iconsArray" />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";

export default {
  name: "App",
  components: {
    Header,
    Main,
  },
  data() {
    return {
      // Elementi del header top
      navItemsArray: [
        {
          text: "Home",
          url: "#",
        },
        {
          text: "Courses",
          url: "#",
        },
        {
          text: "Istructor",
          url: "#",
        },
        {
          text: "Events",
          url: "#",
        },
        {
          text: "Pages",
          url: "#",
        },
        {
          text: "Elements",
          url: "#",
        },
      ],
      // Icone del main top
      iconsArray: [
        {
          img: "h5-custom-icon-1.png",
          text: "Languages",
        },
        {
          img: "h5-custom-icon-2.png",
          text: "Software",
        },
        {
          img: "h5-custom-icon-3.png",
          text: "Business",
        },
        {
          img: "h5-custom-icon-4.png",
          text: "Chemistry",
        },
        {
          img: "h5-custom-icon-5.png",
          text: "Science",
        },
        {
          img: "h5-custom-icon-6.png",
          text: "DIY&Craft",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "./styles/general";
</style>
