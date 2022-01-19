<template>
  <section>
    <!--First Row Card -->
    <div class="my_container">
      <div class="container_icons">
        <div v-for="(icon, index) in iconsArray" :key="index" class="my_icons">
          <img :src="require(`../assets/img/${icon.img}`)" :alt="icon.text" />
          <h3>{{ icon.text }}</h3>
        </div>
      </div>
      <div>
        <h2>
          The Trusted Name <br />
          for In-Home Tutoring.
        </h2>
        <p>
          Lorem ipsum, dolor sit amet consectetur adipisicing elit. Officiis
          autem, eveniet omnis fugiat alias excepturi, magni doloremque
          similique fuga quae rerum minus voluptatibus, et minima tempore
          laudantium optio temporibus voluptas?
        </p>
        <p class="my_more">LEARN MORE</p>
      </div>

      <!-- Primo Jumbotron -->
      <div class="students_image">
        <img src="../assets/img/h5-img-1.jpg" alt="Image of students" />
        <div class="top_page">
          <i class="fas fa-angle-up"></i>
          top
        </div>
      </div>

      <!-- Secondo Jumbotron -->
      <div class="globe_image">
        <div class="my_globe">
          <img src="../assets/img/h5-img-2.jpg" alt="Globe image" />
        </div>
        <div class="globe_txt">
          <h2>
            Empowering <br />
            Children to Reach <br />
            Their Potential
          </h2>
          <p>
            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Quos
            accusamus, alias rerum expedita commodi illum consequuntur? Sapiente
            consectetur vitae repellendus facere dolorem mollitia suscipit quae
            ducimus, quasi ab veritatis officia!
          </p>
          <div class="globe_data_container">
            <div class="globe_data">
              <p>168</p>
              <strong>User Stories</strong>
            </div>
            <div class="globe_data">
              <p>347</p>
              <strong>Events</strong>
            </div>
          </div>
        </div>
        <div class="top_page">
          <i class="fas fa-angle-up"></i>
          top
        </div>
      </div>
    </div>

    <!-- Terzo Jumbotron -->
    <div class="review_zone">
      <div class="reviewer">
        <img src="../assets/img/testimonials-standard-2.png" alt="" />
      </div>
      <div class="review_txt">
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Excepturi,
          eum praesentium aliquam molestias voluptas deleniti, suscipit, maxime
          quo nostrum natus rem cum voluptatum repellat eligendi vero cumque.
          Harum, inventore ex! aliquam molestias voluptas deleniti
        </p>
      </div>
      <div class="reviewer_name">Joan Collins</div>
      <div class="reviewer_class">STUDENT</div>
      <div class="zone_bottom">
        <div v-for="n in 3" :key="n" class="my_circle">
          <div class="my_pointer"></div>
        </div>
      </div>
    </div>

    <!-- Programs of course -->
    <div class="my_container">
      <div class="programs">
        <div class="cells">
          <div
            v-for="(program, index) in programsCourseArray"
            :key="index"
            class="rows"
          >
            <div :class="{ active: program.status }"></div>
            <p class="program_title">{{ program.title }}</p>
          </div>
        </div>
        <div class="program_description">
          <h2>Learning Possibilities</h2>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Ex
            accusamus excepturi consequatur vel, amet optio temporibus nobis
            reiciendis? Laudantium quaerat tempora, id natus quasi possimus esse
            rem molestias ullam minima. Lorem ipsum dolor, sit amet consectetur
            adipisicing elit. Autem consequatur odit repellat accusantium iste
            modi. Adipisci facere doloremque aliquam debitis magni? Neque ullam
            molestias mollitia ducimus deserunt eligendi assumenda porro!
          </p>
          <ul class="program_points_list">
            <li v-for="(point, index) in programsPointsArray" :key="index">
              <i class="fas fa-check"></i>
              {{ point.point }}
            </li>
          </ul>
          <div class="icona">
            <img
              class="w-100"
              src="../assets/img/h12-tabs-icon-1.png"
              alt="icon"
            />
          </div>
        </div>
        <div class="top_page">
          <i class="fas fa-angle-up"></i>
          top
        </div>
      </div>
    </div>

    <!-- Popular Course -->
    <div class="popular_course_section">
      <div class="my_container">
        <div class="text-center w-50 m-auto pt-5">
          <h2>Popular Online Course</h2>
          <p class="pt-5">
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eaque,
            assumenda, non ducimus hic, similique voluptate illum totam vero
            saepe earum repellat modi cum repudiandae est numquam nemo dolorum
            eligendi repellendus.
          </p>
        </div>
        <div class="images_course_container">
          <div
            class="image_course"
            v-for="(image, index) in imagesPopularCourseArray"
            :key="index"
          >
            <img :src="require('../assets/img/' + image)" alt="Course Image" />
          </div>
        </div>
      </div>
      <div class="zone_bottom">
        <div v-for="n in 3" :key="n" class="my_circle_special">
          <div class="my_pointer"></div>
        </div>
      </div>
      <div class="top_page">
        <i class="fas fa-angle-up"></i>
        top
      </div>
    </div>

    <!-- Pricing Table -->
    <PricingTable />

    <!-- Logos Row -->
    <div class="my_container">
      <div class="container_logo">
        <div class="my_logo">
          <div v-for="(logo, index) in logoArray" :key="index">
            <img
              :src="require(`../assets/img/${logo.img}`)"
              alt="University Logo"
            />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import PricingTable from "./PricingTable.vue";
export default {
  name: "Main",
  props: {
    iconsArray: Array,
    programsCourseArray: Array,
    programsPointsArray: Array,
    imagesPopularCourseArray: Array,
    logoArray: Array,
  },
  components: {
    PricingTable,
  },
};
</script>

<style lang="scss" scoped>
@import "../styles/variables";
// Row card
.container_icons {
  display: flex;
  justify-content: space-between;
  margin-top: 50px;
  margin-bottom: 100px;
  .my_icons {
    background-color: $card_color;
    height: 250px;
    width: 200px;
    display: flex;
    flex-direction: column;
    align-items: center;

    img {
      margin: 40px 0;
    }
  }
}
// Primo Jumbotron
.students_image {
  position: relative;
  margin: 80px 0;
}
// Secondo Jumbotron
.globe_image {
  display: flex;
  position: relative;
  .my_globe {
    width: 50%;
    img {
      width: 100%;
    }
  }
  .globe_txt {
    width: 50%;
    padding: 0 100px;
    .globe_data_container {
      width: 70%;
      display: flex;
      justify-content: space-between;
      align-items: flex-start;

      .globe_data {
        line-height: 50px;
        color: $my_secondary_color;
        p {
          font-size: 60px;
        }
        strong {
          font-size: 30px;
        }
      }
    }
  }
}
// Terzo Jumbotron
.review_zone {
  margin: 80px 0;
  text-align: center;
  position: relative;
  background-image: url("../assets/img/h5-parallax-img-1.png");
  background-size: cover;
  height: 600px;
  color: $my_primary_color;
  .reviewer {
    padding-top: 150px;
  }
  .review_txt {
    width: 50%;
    margin: 30px auto;
  }
}
// Programs of course
.programs {
  width: 95%;
  height: 700px;
  margin: 100px;
  display: flex;
  justify-content: space-between;
  position: relative;
  ul {
    padding-left: 0;
  }
  .cells {
    width: 40%;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    .rows {
      width: 60%;
      height: 100px;
      border: 3px solid $grid_color;
      display: flex;
      align-items: center;
      :hover,
      .active {
        color: $my_secondary_color;
        border-left: 10px solid $my_secondary_color;
        height: 100%;
        padding-left: 20px;
        display: flex;
        align-items: center;
      }
      .program_title {
        padding-left: 30px;
        font-weight: bold;
        color: $main_txt_color;
        font-size: 20px;
      }
    }
  }
  .program_description {
    width: 60%;
    height: 100%;
    margin: 100px 0;
    position: relative;
    .program_points_list {
      margin-top: 50px;
      line-height: 50px;
      font-size: 20px;
      .fa-check {
        font-size: 15px;
        color: $my_secondary_color;
      }
    }
  }
  .icona {
    position: absolute;
    width: 120px;
    bottom: 40%;
    right: 5%;
  }
}
// Popular Course
.popular_course_section {
  border-top: 2px solid lightgray;
  border-bottom: 1px solid lightgray;
  background-image: url("../assets/img/background-pattern.jpg");
  height: 1200px;
  position: relative;
  .images_course_container {
    display: flex;
    justify-content: space-between;
    margin: 100px;
    padding-right: 20px;
    .image_course {
      width: 300px;
      height: 400px;
      background-color: pink;
    }
  }
  .my_circle_special {
    width: 20px;
    height: 20px;
    border-radius: 50%;
    margin: 70px 5px;
    background-color: $my_secondary_color;
  }
}
// Logos Row
.container_logo {
  position: relative;
  .my_logo {
    height: 300px;

    display: flex;
    justify-content: space-between;
    align-items: center;
  }
}
</style>