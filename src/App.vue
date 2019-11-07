<template>
  <v-app>
    <v-app-bar :light="true" color="white darken-2" app>
      <v-toolbar-title>
        <v-img width="140" src="./assets/logo.png"></v-img>
      </v-toolbar-title>
      <div class="flex-grow-1"></div>
      <v-toolbar-items class="mr-8">
        <v-btn text>Link 1</v-btn>
        <v-btn text>Link 2</v-btn>
        <v-btn text>Link 3</v-btn>
      </v-toolbar-items>
      <v-btn icon>
        <v-badge :left="true" color="green accent-4">
          <template v-slot:badge>0</template>
          <v-icon color="orange darken-2">mdi-cart</v-icon>
        </v-badge>
      </v-btn>
      <v-btn icon>
        <v-icon color="orange darken-2">mdi-account</v-icon>
      </v-btn>
    </v-app-bar>
    <v-content class="sabor-fit">
      <v-container fluid>asdfasdffadfs</v-container>
    </v-content>
  </v-app>
</template>

<script>
export default {
  name: "App",

  components: {},

  data: () => ({
    logo: ""
  })
};
</script>

<style lang="scss" scoped>
.sabor-fit {
  background-image: url("./assets/bg-sabor-fit.png");
  background-repeat: repeat-x;
}
</style>