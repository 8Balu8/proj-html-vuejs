<template>
  <div class="box_table">
    <div class="container_table_price">
      <div class="my_container">
        <div class="description">
          <h2>Pricing Plans</h2>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Molestiae
            deserunt aspernatur suscipit incidunt consequatur maiores
          </p>
        </div>
        <div class="my_table">
          <!-- Colonna Options -->
          <div class="col_options">
            <div class="promo bg_table">Save up to 40% by paying weekly</div>
            <div
              v-for="(option, index) in tableOptions"
              :key="index"
              class="option"
            >
              {{ option.title }}
            </div>
          </div>
          <!-- Colonna Plans -->
          <div
            class="col_options"
            v-for="(plan, index) in subscriptionType"
            :key="index"
          >
            <div class="name_plan bg_table">
              <img
                class="w-50"
                :src="require(`../assets/img/${plan.img}`)"
                alt="Image Plan"
              />
              <p>{{ plan.type }}</p>
              <span>{{ plan.price }}</span>
            </div>
            <div class="option">{{ plan.numberOfCourses }}</div>
            <div class="option">{{ plan.time }}</div>
            <div class="option">
              <i :class="plan.webDes ? 'fas fa-check' : 'fas fa-times'"></i>
            </div>
            <div class="option">
              <i :class="plan.humCentDes ? 'fas fa-check' : 'fas fa-times'"></i>
            </div>
            <div class="option">
              <i :class="plan.basicMark ? 'fas fa-check' : 'fas fa-times'"></i>
            </div>
            <div class="option">
              <i
                :class="plan.pythForEvery ? 'fas fa-check' : 'fas fa-times'"
              ></i>
            </div>
            <div class="option">
              <i :class="plan.androidDev ? 'fas fa-check' : 'fas fa-times'"></i>
            </div>
            <div class="option">
              <i
                :class="plan.businEnglish ? 'fas fa-check' : 'fas fa-times'"
              ></i>
            </div>
            <div class="btn_contain bg_table">
              <button type="button" class="btn btn-primary p-3">
                GET IT NOW
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "PricingTable",
  data() {
    return {
      tableOptions: [
        {
          title: "Number of Courses",
        },
        {
          title: "Time",
        },
        {
          title: "Web Designing",
        },
        {
          title: "Human-Centered Design",
        },
        {
          title: "Basic Marketing",
        },
        {
          title: "Python for Everybody",
        },
        {
          title: "Android Developer",
        },
        {
          title: "Business English",
        },
      ],
      subscriptionType: [
        {
          img: "h5-custom-icon-7.png",
          type: "Standard",
          price: "$12",
          numberOfCourses: "2",
          time: "15 Days",
          webDes: true,
          humCentDes: true,
          basicMark: false,
          pythForEvery: false,
          androidDev: false,
          businEnglish: false,
        },
        {
          img: "h5-custom-icon-8.png",
          type: "Professional",
          price: "$59",
          numberOfCourses: "4",
          time: "30 Days",
          webDes: true,
          humCentDes: true,
          basicMark: true,
          pythForEvery: true,
          androidDev: false,
          businEnglish: false,
        },
        {
          img: "h5-custom-icon-9.png",
          type: "Advance",
          price: "$88",
          numberOfCourses: "6",
          time: "30 Days",
          webDes: true,
          humCentDes: true,
          basicMark: true,
          pythForEvery: true,
          androidDev: true,
          businEnglish: true,
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../styles/variables";
.box_table {
  border-bottom: 1px solid lightgray;
  .container_table_price {
    background-image: url("../assets/img/background-pattern.jpg");
    padding-bottom: 100px;
    .description {
      text-align: center;
      h2 {
        margin: 50px 0;
      }
      p {
        margin: 50px 0;
      }
    }
    .my_table {
      display: flex;
      .col_options {
        width: calc(100% / 4);
        .promo {
          border: 1px solid $grid_color;
          border-top: 2px solid $my_secondary_color;
          width: 100%;
          height: 300px;
          display: flex;
          align-items: flex-end;
          padding: 50px;
          font-size: 30px;
        }
        .option {
          border: 1px solid $grid_color;
          height: 100px;
          display: flex;
          align-items: center;
          justify-content: center;
          font-size: 25px;
          background-color: $my_primary_color;
        }
        .name_plan {
          border: 3px solid $grid_color;
          border-top: 2px solid $my_secondary_color;
          width: 100%;
          height: 300px;
          display: flex;
          flex-direction: column;
          align-items: center;
          padding: 50px;
          font-size: 30px;

          &:hover {
            border-top: 10px solid $my_secondary_color;
          }
        }
        .btn_contain {
          border: 1px solid $grid_color;
          height: 100px;
          display: flex;
          align-items: center;
          justify-content: center;
        }
      }
      .bg_table {
        background-color: $bg_table_price;
      }
    }
  }
}
</style>