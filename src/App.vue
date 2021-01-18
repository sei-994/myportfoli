<template>
  <v-app>
    <!-- header -->
    <AppHeader />
    <!-- content -->
    <v-content
      ><!-- トップページのコンポーネントは必ずv-contentでくくる -->
      <Home></Home>
    </v-content>
    <!-- footer -->
    <AppFooter />
  </v-app>
</template>

<script>
import AppHeader from "./components/AppHeader"
import AppFooter from "./components/AppFooter"
import Home from "./components/Home"

export default {
  name: "App",

  components: {
    AppHeader,
    Home,
    AppFooter,
  },
}
</script>

<style lang="scss" scoped>
// tabs CSS修正
.v-toolbar__title {
  overflow: visible !important;
  margin-right: 50px !important;
}
</style>
