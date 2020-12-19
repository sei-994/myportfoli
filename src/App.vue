<template>
  <v-app>
    <!-- ここにヘッダーをコーディング -->
    <header>
      <v-app-bar app dark>
        <!-- ここから追加 -->
        <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>
        <!-- ここまで追加 -->
        <v-toolbar-title>MyPortfolioSite</v-toolbar-title>
      </v-app-bar>
      <v-navigation-drawer v-model="drawer" fixed temporary>
        <v-list nav dense>
          <v-list-item-group>
            <v-list-item>
              <v-list-item-title>
                Home
              </v-list-item-title>
            </v-list-item>
            <v-list-item>
              <v-list-item-title>
                About
              </v-list-item-title>
            </v-list-item>
            <v-list-item>
              <v-list-item-title>
                Work
              </v-list-item-title>
            </v-list-item>
            <v-list-item>
              <v-list-item-title>
                Service
              </v-list-item-title>
            </v-list-item>
          </v-list-item-group>
        </v-list>
      </v-navigation-drawer>
    </header>
    <Home></Home>
  </v-app>
</template>

<script>
import Home from "./components/Home"

export default {
  name: "App",

  components: {
    Home,
  },

  data() {
    return {
      drawer: false,
    }
  },
}
</script>
