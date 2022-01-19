<template>
  <div id="app">
    <Header :navItemsArray="navItemsArray" />
    <Main
      :iconsArray="iconsArray"
      :programsCourseArray="programsCourseArray"
      :programsPointsArray="programsPointsArray"
      :imagesPopularCourseArray="imagesPopularCourseArray"
    />
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
      // Elementi del navbar in header top
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
      // Icone delle card main top
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
      // Lista programmi del corso di Main
      programsCourseArray: [
        {
          title: "What We Do",
          status: true,
        },
        {
          title: "Degree Programme",
          status: false,
        },
        {
          title: "Career Achievements",
          status: false,
        },
        {
          title: "Personal Managment",
          status: false,
        },
        {
          title: "Steps To Success",
          status: false,
        },
        {
          title: "Knowledge Transfer",
          status: false,
        },
      ],
      // Dettagli del programma del corso
      programsPointsArray: [
        {
          point: "We enrich lives through learning.",
        },
        {
          point: "Maximizing potential through individual attention.",
        },
        {
          point: "The trusted name for specialized training.",
        },
        {
          point: "People thach. People learn. This is where they connect.",
        },
      ],
      // Immagini di Popular Course
      imagesPopularCourseArray: [
        "landing-carousel-gallery-img-1.jpg",
        "landing-carousel-gallery-img-2.jpg",
        "landing-carousel-gallery-img-3.jpg",
        // "landing-carousel-gallery-img-4.jpg",
        // "landing-carousel-gallery-img-5.jpg",
        // "landing-carousel-gallery-img-7.jpg",
      ],
    };
  },
};
</script>

<style lang="scss">
@import "./styles/general";
</style>
