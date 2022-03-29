<template>
  <footer>
    <div class="Footer">
      <div class="main_container">
        <div class="cities">
          <h1>ГОРОДА</h1>
          <div v-for="(city, idx) in cities" :key="'A' + idx">
            <p>{{ city.title }}</p>
          </div>
        </div>
        <div class="stations">
          <h1>АВТОВОКЗАЛЫ</h1>
          <div v-for="(station, idx) in stations" :key="'B' + idx">
            <p>{{ station.title }}</p>
          </div>
        </div>
        <div class="directions">
          <h1>НАПРАВЛЕНИЯ</h1>
          <div v-for="(direction, idx) in directions" :key="'C' + idx">
            <p>{{ direction.title }}</p>
          </div>
        </div>
        <div class="social_media">
          <h1>СОЦИАЛЬНЫЕ СЕТИ</h1>
          <div class="links mb-7">
            <div v-for="(img, idx) in networks" :key="'D' + idx">
              <img :src="img.img" />
            </div>
          </div>
          <img src="@/assets/images/Footer/2.png" class="apps mb-6" />
          <img src="@/assets/images/Footer/1.png" class="apps" />
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  data: () => ({
    cities: [
      {
        title: "Алматы",
      },
      {
        title: "Нур-Султан",
      },
      {
        title: "Актау",
      },
      {
        title: "Атырау",
      },
      {
        title: "Усть-Каменогорск",
      },
      {
        title: "Семей",
      },
      {
        title: "Караганда",
      },
    ],
    stations: [
      {
        title: "Сайран",
      },
      {
        title: "Саяхат",
      },
      {
        title: "Талгар",
      },
      {
        title: "Райымбек батыра",
      },
      {
        title: "Сапаржай",
      },
      {
        title: "Шарын",
      },
      {
        title: "Астана",
      },
    ],
    directions: [
      {
        title: "Алматы - Нур-Султан",
      },
      {
        title: "Семей - Актау",
      },
      {
        title: "Нур-Султан - Атырау",
      },
      {
        title: "Усть-Каменогорск - Алматы",
      },
      {
        title: "Павлодар - Семей",
      },
      {
        title: "Актау - Шымкент",
      },
      {
        title: "Тараз - Алматы",
      },
    ],
    networks: [
      {
        img: require("@/assets/images/Footer/facebook.png"),
      },
      {
        img: require("@/assets/images/Footer/ok.png"),
      },
      {
        img: require("@/assets/images/Footer/telegram.png"),
      },
      {
        img: require("@/assets/images/Footer/vk.png"),
      },
      {
        img: require("@/assets/images/Footer/insta.png"),
      },
    ],
  }),
};
</script>

<style lang="scss" scoped>
.Footer {
  background: #fff;
}
.main_container {
  display: flex;

  padding: 26px 0 60px;

  h1 {
    font-family: "Roboto-Bold";
    font-style: normal;
    font-weight: 500;
    font-size: 16px;
    line-height: 19px;
    color: #0d131c;
    margin-bottom: 20px;
  }
  p {
    font-family: "Roboto-Regular";
    font-style: normal;
    font-weight: 400;
    font-size: 15px;
    line-height: 19px;
    color: #0d131c;
    margin-bottom: 12px !important;
  }
  .stations {
    margin: 0 68px;
  }
  .directions {
    max-width: 211px;
    width: 100%;
  }
  .social_media {
    margin-left: 85px;
    display: flex;
    flex-direction: column;

    .links {
      display: flex;
      align-items: center;

      img {
        margin-right: 15px;
      }
    }
    .apps {
      width: 186px;
      height: 50px;
    }
  }
}
</style>