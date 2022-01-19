<template>
  <div id="app">
    <Header :navItemsArray="navItemsArray" />
    <Main
      :iconsArray="iconsArray"
      :programsCourseArray="programsCourseArray"
      :programsPointsArray="programsPointsArray"
      :imagesPopularCourseArray="imagesPopularCourseArray"
      :logoArray="logoArray"
    />
    <Footer
      :menu1links="menu1links"
      :menu2links="menu2links"
      :menu3links="menu3links"
    />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Header,
    Main,
    Footer,
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
      // Loghi Main End
      logoArray: [
        {
          img: "h5-client-5.png",
        },
        {
          img: "h5-client-1.png",
        },
        {
          img: "h5-client-2.png",
        },
        {
          img: "h5-client-1.png",
        },
      ],
      // Elementi del Footer
      menu1links: [
        {
          txt: "Providing Life Changing",
          txt1: "Experiences Through",
          txt2: "Education Class That Fit your",
          txt3: "Busy Life. Closer to Home",
        },
        {
          txt: "1-677-124-44227",
        },
        {
          txt: "Mon - Sat 8.00 - 18:00",
        },
      ],
      menu2links: [
        {
          txt: "Business English",
          name: "Preston Marshall",
        },
        {
          txt: "Social Computing",
          name: "David Sanders",
        },
        {
          txt: "Learn Spanish",
          name: "Jennie King",
        },
      ],
      menu3links: [
        {
          txt: "User dashboard",
        },
        {
          txt: "Contact Us",
        },
        {
          txt: "FAQ",
        },
        {
          txt: "Course Offer",
        },
        {
          txt: "Events",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "./styles/general";
</style>
