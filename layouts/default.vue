<template>
  <v-app>
    <vue-header />
    <nuxt />
    <vue-footer />
  </v-app>
</template>

<script>
import VueFooter from "../components/ui/VueFooter.vue";
import vueHeader from "../components/ui/vueHeader.vue";
export default {
  components: { vueHeader, VueFooter },
};
</script>

<style lang="scss" scoped>
.theme--light.v-application {
  background: #2e7094;
}
</style>