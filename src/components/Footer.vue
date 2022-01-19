<template>
  <footer>
    <div class="my_container">
      <div class="footer_link">
        <div class="my_menu">
          <img src="../assets/img/logo-light.png" alt="iAcademy Logo" />
          <div class="links" v-for="(link, index) in menu1links" :key="index">
            <p>{{ link.txt }}</p>
            <p>{{ link.txt1 }}</p>
            <p>{{ link.txt2 }}</p>
            <p>{{ link.txt3 }}</p>
          </div>
        </div>
        <div class="my_menu_central">
          <h4>Popular Courses</h4>
          <div class="links" v-for="(link, index) in menu2links" :key="index">
            <h5>{{ link.txt }}</h5>
            <p>{{ link.name }}</p>
          </div>
        </div>
        <div class="my_menu_central">
          <h4>Support</h4>
          <div class="links">
            <p v-for="(link, index) in menu3links" :key="index">
              {{ link.txt }}
            </p>
          </div>
        </div>
        <div class="learning_area_maps">
          <h4>Flexible Learning</h4>
          <img src="../assets/img/footer-img-1.png" alt="Globe Image" />
        </div>
      </div>
      <div class="footer_bottom">
        <div>
          <p>Copyrights 2017 ©Mikado Themes</p>
        </div>
        <div class="contacts">
          <p>CALL +44 300 303 0266</p>
          <p>FOLLOW US</p>
          <div class="socials">
            <a href="#">
              <i class="fab fa-twitter"></i>
            </a>
            <a href="#">
              <i class="fab fa-instagram"></i>
            </a>
            <a href="#">
              <i class="fab fa-facebook-f"></i>
            </a>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
  props: {
    menu1links: Array,
    menu2links: Array,
    menu3links: Array,
  },
};
</script>

<style lang="scss" scoped>
footer {
  background-color: #222222;
  color: white;
  .footer_link {
    padding-top: 100px;
    display: flex;
    justify-content: space-between;
    .my_menu {
      width: 20%;
      img {
        width: 60%;
        margin-bottom: 50px;
      }
      .links {
        margin-bottom: 30px;
      }
    }
    .my_menu_central {
      margin: 0 30px;
      h4 {
        margin-bottom: 50px;
      }
    }
    .learning_area_maps {
      text-align: end;

      h4 {
        margin-bottom: 40px;
        margin-right: 30px;
      }
      img {
        width: 50%;
      }
    }
  }
  .footer_bottom {
    border-top: 1px solid white;
    display: flex;
    justify-content: space-between;
    padding: 40px 0;
    .contacts {
      width: 40%;
      display: flex;
      justify-content: space-around;
    }
    .socials {
      i {
        margin: 0 10px;
      }
    }
  }
}

p,
h5,
a {
  color: white;
  cursor: pointer;
  &:hover {
    text-decoration: underline white;
  }
}
</style>