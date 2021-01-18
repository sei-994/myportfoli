<template>
  <header>
    <v-app-bar app dark>
      <!-- hambargr-menu -->
      <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>

      <!-- header-title -->
      <v-toolbar-title>MyPortfolioSite</v-toolbar-title>
      <!-- タブ追加（パソコン用） -->
      <v-tabs>
        <v-tab
          v-for="(menuItem, index) in menuItems"
          :key="index"
          :to="menuItem.url"
        >
          {{ menuItem.name }}</v-tab
        >
      </v-tabs>
    </v-app-bar>
    <v-navigation-drawer v-model="drawer" fixed temporary>
      <v-list nav dense>
        <v-list-item-group>
          <v-list-item
            v-for="(menuItem, Index) in menuItems"
            :key="Index"
            to="menuItem.url"
          >
            <v-list-item-title>
              {{ menuItem.name }}
            </v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
  </header>
</template>

<script>
import constants from "../common/constants.js"
export default {
  name: "AppHeader",
  data() {
    return {
      drawer: false,
      menuItems: constants.menuItems,
    }
  },
}
</script>

<style></style>
