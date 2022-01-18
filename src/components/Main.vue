<template>
  <section>
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
        <img src="../assets/img/h5-img-1.jpg" alt="" />
        <div class="top_page">
          <i class="fas fa-angle-up"></i>
          top
        </div>
      </div>
      <!-- Secondo Jumbotron -->
      <div class="globe_image">
        <div class="my_globe">
          <img src="../assets/img/h5-img-2.jpg" alt="" />
        </div>
        <div class="globe_txt">
          <h1>
            Empowering <br />
            Children to Reach <br />
            Their Potential
          </h1>
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
          "Lorem ipsum dolor sit amet consectetur adipisicing elit. Excepturi,
          eum praesentium aliquam molestias voluptas deleniti, suscipit, maxime
          quo nostrum natus rem cum voluptatum repellat eligendi vero cumque.
          Harum, inventore ex! aliquam molestias voluptas deleniti"
        </p>
      </div>
      <div class="reviewer_name">Joan Collins</div>
      <div class="reviewer_class">STUDENT</div>
      <div class="review_zone_bottom">
        <div v-for="n in 3" :key="n" class="my_circle">
          {{ n.my_circle }}
          <div class="my_pointer"></div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
// import icons from '../data/icons.js'
export default {
  name: "Main",
  props: {
    iconsArray: Array,
  },
};
</script>

<style lang="scss" scoped>
@import "../styles/variables";
.container_icons {
  display: flex;
  justify-content: space-between;
  margin-top: 50px;
  margin-bottom: 100px;
  .my_icons {
    background-color: #f2f8fc;
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
.students_image {
  position: relative;
  margin: 80px 0;
}
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
  .review_zone_bottom {
    display: flex;
    justify-content: center;
    margin-top: 100px;
  }
}
</style>