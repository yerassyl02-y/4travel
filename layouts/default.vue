<template>
  <v-app>
    <vue-header />
    <nuxt />
  </v-app>
</template>

<script>
import vueHeader from "../components/ui/vueHeader.vue";
export default {
  components: { vueHeader },
};
</script>

<style lang="scss" scoped>
.theme--light.v-application {
  background: #2e7094;
}
</style>