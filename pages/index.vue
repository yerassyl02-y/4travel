<template>
  <div class="home">
    <div class="content">
      <h1>Ездить стало удобнее и дешевле</h1>
      <p>Лучший способ купить автобусные билеты дешево</p>

      <flight />
    </div>
  </div>
</template>

<script>
import Flight from "../components/Flight.vue";
export default {
  components: { Flight },
};
</script>

<style lang="scss" scoped>
.home {
  background: #2e7094;
  margin-top: 93px;
  height: 670px;
  background: url("@/assets/images/Homepage/background.png");
  background-repeat: no-repeat;
  background-position: left bottom;
  background-size: contain;

  h1 {
    font-family: "Roboto-Bold";
    font-style: normal;
    font-weight: 700;
    font-size: 40px;
    line-height: 47px;
    text-align: center;
    color: #ffffff;
  }
  p {
    margin: 26px 0 74px;
    font-family: "Roboto-Medium";
    font-style: normal;
    font-weight: 500;
    font-size: 16px;
    line-height: 19px;
    text-align: center;
    color: #ffffff;
  }
}
</style>