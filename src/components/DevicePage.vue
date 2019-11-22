<template>
  <v-ons-page>
    <v-ons-list-title>Bemo list</v-ons-list-title>
    <v-ons-card>
      <v-ons-row vertical-align="center">
        <v-ons-col width="50px">
          <img src="../assets/images/bemo1.jpg" alt />
        </v-ons-col>
        <v-ons-col>
          <div class="title">Louis Vuitton Bag</div>
        </v-ons-col>
        <v-ons-col width="50px">
          <v-ons-icon icon="fa-info-circle"></v-ons-icon>
        </v-ons-col>
      </v-ons-row>
    </v-ons-card>
    <v-ons-card>
      <v-ons-row vertical-align="center">
        <v-ons-col width="50px">
          <img src="../assets/images/bemo2.jpg" alt />
        </v-ons-col>
        <v-ons-col>
          <div class="title">Macbook Pro</div>
        </v-ons-col>
        <v-ons-col width="50px">
          <v-ons-icon icon="fa-info-circle"></v-ons-icon>
        </v-ons-col>
      </v-ons-row>
    </v-ons-card>
    <v-ons-fab position="bottom right" visible="true">
      <v-ons-icon icon="fa-plus"></v-ons-icon>
    </v-ons-fab>
  </v-ons-page>
</template>

<script>
export default {
  name: "device",
  data() {
    return {
      msg: "BEMO",
      essentialLinks: [
        {
          label: "Core Docs",
          link: "https://vuejs.org",
          icon: "fa-book"
        },
        {
          label: "Community Chat",
          link: "https://chat.vuejs.org",
          icon: "fa-commenting"
        },
        {
          label: "Forum",
          link: "https://forum.vuejs.org",
          icon: "ion-chatboxes"
        },
        {
          label: "Twitter",
          link: "https://twitter.com/vuejs",
          icon: "fa-twitter"
        },
        {
          label: "Docs for this template",
          link: "http://vuejs-templates.github.io/webpack/",
          icon: "fa-file-text"
        }
      ]
    };
  },
  methods: {
    goTo(url) {
      window.open(url, "_blank");
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.header {
  text-align: center;
}

img {
  width: 50px;
  height: 50px;
}

ons-list-title {
  text-transform: none;
}

ons-list-title:not(:first-of-type) {
  margin-top: 30px;
}

ons-card {
  text-align: center;
}

ons-list-item,
ons-card {
  cursor: pointer;
}
</style>
