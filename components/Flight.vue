<template>
  <div class="Flight">
    <div class="Flight__content">
      <div class="Flight__tours">
        <v-text-field placeholder="Откуда" class="textfield1" />
        <v-text-field placeholder="Куда" class="textfield2 mx-1" />
        <v-menu
          ref="menu"
          v-model="menu1"
          :close-on-content-click="false"
          :return-value.sync="date"
          transition="scale-transition"
          offset-y
          min-width="auto"
        >
          <template v-slot:activator="{ on, attrs }">
            <v-text-field
              class="textfield3"
              v-model="dateFormatted"
              persistent-hint
              v-bind="attrs"
              @blur="date = parseDate(dateFormatted)"
              v-on="on"
            ></v-text-field>
          </template>
          <v-date-picker
            placeholder="Дата выезда"
            v-model="date"
            no-title
            @input="menu1 = false"
          ></v-date-picker>
        </v-menu>
        <img src="@/assets/images/Homepage/calendar.png" />
      </div>
      <v-btn class="find_btn ml-5">Найти билеты</v-btn>
    </div>
  </div>
</template>

<script>
export default {
  data: (vm) => ({
    menu1: false,
    date: new Date(Date.now() - new Date().getTimezoneOffset() * 60000)
      .toISOString()
      .substr(0, 10),
    dateFormatted: vm.formatDate(
      new Date(Date.now() - new Date().getTimezoneOffset() * 60000)
        .toISOString()
        .substr(0, 10)
    ),
    menu1: false,
    menu2: false,
  }),
  computed: {
    computedDateFormatted() {
      return this.formatDate(this.date);
    },
  },

  watch: {
    date(val) {
      this.dateFormatted = this.formatDate(this.date);
    },
  },

  methods: {
    formatDate(date) {
      if (!date) return null;

      const [year, month, day] = date.split("-");
      return `${month}/${day}/${year}`;
    },
    parseDate(date) {
      if (!date) return null;

      const [month, day, year] = date.split("/");
      return `${year}-${month.padStart(2, "0")}-${day.padStart(2, "0")}`;
    },
  },
};
</script>

<style lang="scss" scoped>
.Flight {
  width: 100%;

  &__content {
    max-width: 800px;
    width: 100%;

    display: flex;
    align-items: center;

    margin: 0 auto;

    .textfield1 {
      border-top-left-radius: 5px;
      border-bottom-left-radius: 5px;
    }
    .textfield3 {
      border-top-right-radius: 5px;
      border-bottom-right-radius: 5px;
    }
  }
  &__tours {
    display: flex;
    align-items: center;
    position: relative;

    img {
      object-fit: cover;
      width: 16px;
      height: 16px;
      position: absolute;
      right: 25px;
      top: 25px;
    }
  }
}
</style>