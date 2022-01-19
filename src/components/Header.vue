<template>
  <header>
    <!-- Header Slider -->
    <div class="bg_Header" :style="bgImage">
      <!--Header top Navbar -->
      <div class="my_container header_top">
        <div class="logo">
          <img src="../assets/img/logo-light.png" alt="iAcademy Logo" />
        </div>
        <div class="nav_items">
          <div class="item" v-for="(items, i) in navItemsArray" :key="i">
            <a :href="`${items.url}`">{{ items.text }}</a>
          </div>
        </div>
        <div class="nav_icons">
          <i class="fas fa-search"></i>
          <i class="far fa-clipboard">
            <div class="counter">0</div>
          </i>
          <i class="fas fa-bars"></i>
        </div>
      </div>
      <!-- Header Center Call to action -->
      <div class="header_center">
        <h1>Contemporary Ideas</h1>
        <p>
          Lorem, ipsum dolor sit amet consectetur adipisicing elit. Eligendi
          quis natus totam veniam, commodi dolorum inventore, deleniti quasi
          laborum obcaecati blanditiis libero voluptatem error aut repudiandae
          facilis architecto ex? Blanditiis?
        </p>
        <div>
          <button class="my_btn">Register Now</button>
        </div>
      </div>
      <!-- Header bottom circle for number page -->
      <div class="header_bottom">
        <div
          v-for="(n, i) in carouselImgArray.length"
          :key="n"
          class="my_circle"
        >
          <div :class="{ my_pointer: imageSelected === i }"></div>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
  props: {
    navItemsArray: Array,
  },
  data: function () {
    return {
      imageSelected: 0,
      carouselImgArray: [
        "course-9-f-img.jpg",
        "course-1-f-img.jpg",
        "course-4-f-img.jpg",
        "course-2-f-img.jpg",
      ],
    };
  },
  computed: {
    bgImage() {
      return {
        backgroundImage: `url${require("../assets/img/" +
          this.carouselImgArray[this.imageSelected])}`,
      };
    },
  },
  methods: {
    increaseImageSelected: function () {
      if (this.imageSelected < this.carouselImgArray.length - 1) {
        this.imageSelected++;
      } else {
        this.imageSelected = 0;
      }
    },
    autoNextImage: function () {
      this.autoIncreaseImageSelected = setInterval(() => {
        this.increaseImageSelected();
      }, 2000);
    },
  },
  created() {
    // timing function che incrementa indice contenuto in imageSelected MA dentro le dimensioni dell'array
    this.autoNextImage();
  },
};
</script>


<style scoped lang="scss">
@import "../styles/variables";
.bg_Header {
  width: 100%;
  height: 900px;
  background-image: url("../assets/img/course-9-f-img.jpg");
  background-size: cover;
  background-position: center;

  .header_top {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding-top: 20px;

    .logo {
      width: 250px;
      cursor: pointer;

      img {
        width: 100%;
      }
    }
    .nav_items {
      width: calc(100% - 500px);
      display: flex;
      align-items: center;

      .item {
        margin: auto;

        a {
          text-decoration: none;
          text-transform: uppercase;
          color: white;
          font-size: 20px;

          &:hover {
            font-weight: bold;
          }
        }
      }
    }
    .nav_icons {
      width: 250px;
      display: flex;
      align-items: center;
      justify-content: space-around;
      .fas,
      .far {
        font-size: 26px;
        color: white;
        cursor: pointer;
      }
      .fa-search {
        transform: scaleX(-1);
      }
      .fa-clipboard {
        position: relative;
        color: white;
      }
      .counter {
        position: absolute;
        top: 0;
        right: 0;
        transform: translate(60%, -20%);
        width: 15px;
        height: 15px;
        border-radius: 50%;
        background: #40c4fe;
        font-size: 12px;
        display: flex;
        justify-content: center;
        align-items: center;
      }
    }
  }
  .header_center {
    position: absolute;
    width: 80%;
    margin: 0 auto;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    text-align: center;

    h1 {
      font-size: 90px;
      margin-bottom: 30px;
      color: white;
    }

    p {
      margin-bottom: 30px;
      color: white;
    }

    .my_btn {
      padding: 20px 40px;
      color: white;
      background-color: #40c4fe;
      border: none;
      text-transform: uppercase;
      font-size: 16px;
      font-weight: bold;
    }
  }
  .header_bottom {
    position: absolute;
    bottom: 0;
    width: 100%;
    height: 100px;
    display: flex;
    justify-content: center;
    align-items: flex-end;
  }
}
</style>


