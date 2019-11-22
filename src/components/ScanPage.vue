<template>
  <v-ons-page>
    <v-ons-list-title>Scan</v-ons-list-title>
    <div class="header">
      <img src="../assets/onsenui-logo.png">
    </div>
  </v-ons-page>
</template>

<script>
export default {
  name: 'scan',
  data () {
    return {

    }
  },
  methods: {

  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.header {
  text-align: center;
  margin-bottom: 20px;
}

img {
  max-width: 150px;
}

ons-list-title {
  text-transform: none;
}

ons-list-item {
  cursor: pointer;
}
</style>
