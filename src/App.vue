<template>
  <v-ons-page id="app">
    <v-ons-toolbar>
      <div class="center">{{ title }}</div>
    </v-ons-toolbar>

    <v-ons-tabbar swipeable position="auto" :tabs="tabs" :visible="true" :index.sync="activeIndex"></v-ons-tabbar>
  </v-ons-page>
</template>

<script>
import HomePage from "./components/HomePage";
import DevicePage from "./components/DevicePage";
import ScanPage from "./components/ScanPage";
import SettingPage from "./components/SettingPage";

export default {
  name: "app",
  data() {
    return {
      activeIndex: 0,
      tabs: [
        {
          icon: "fa-home",
          label: "Home",
          page: HomePage,
          props: {
            myProp: "This is a page prop!"
          },
          badge: 7,
          key: "homePage"
        },
        {
          icon: "fa-tag",
          label: "My Bemo",
          page: DevicePage,
          props: {
            myProp: "This is a page prop!"
          },
          key: "devicePage"
        },
        {
          icon: "fa-search-location",
          label: "Search for Bemo",
          page: ScanPage,
          key: "scanPage"
        },
        {
          icon: "fa-tools",
          label: "Settings",
          page: SettingPage,
          key: "settingPage"
        }
      ]
    };
  },
  computed: {
    title() {
      return this.tabs[this.activeIndex].label;
    }
  },
  components: {
    HomePage,    
    DevicePage,
    ScanPage,
    SettingPage
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
ons-splitter-side[side="left"][animation="overlay"] {
  border-right: 1px solid #bbb;
}
</style>
