<template>
  <v-app style="height:2500px">
    <v-navigation-drawer class="d-flex d-sm-none" v-model="drawer" :mini-variant="variant" app>
      <v-list-item class="pb-3">
        <v-list-item-content>
          <v-list-item-title class="text-center">SABOR FIT</v-list-item-title>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list>
        <v-list-item-group color="blue-grey lighten-2">
          <v-list-item link class="font-weight-light">
            <v-list-item-content>link 1</v-list-item-content>
          </v-list-item>
          <v-list-item link class="font-weight-light">
            <v-list-item-content>link 2</v-list-item-content>
          </v-list-item>
          <v-list-item link class="font-weight-light">
            <v-list-item-content>link 3</v-list-item-content>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar :light="true" color="white darken-2" app>
      <v-app-bar-nav-icon class="d-flex d-sm-none" @click="toggleDrawer()"></v-app-bar-nav-icon>
      <v-toolbar-title>
        <v-img width="140" src="./assets/logo.png"></v-img>
      </v-toolbar-title>
      <div class="flex-grow-1"></div>
      <v-toolbar-items class="mr-8 d-none d-sm-flex">
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
      <v-container fluid>asdfasasdfasdfasdfdffadfs</v-container>
    </v-content>
  </v-app>
</template>

<script>
export default {
  name: "App",

  components: {},

  data: () => ({
    drawer: false,
    variant: false,
    classHeader: true,
    permanentValue: false
  }),
  mounted() {
    this.onResize();
  },
  methods: {
    toggleDrawer() {
      this.drawer = !this.drawer;
    },
    onResize() {
      let screenSize = innerWidth;
      if (screenSize > 768) this.permanentValue = true;
      else this.permanentValue = false;
    }
  }
};
</script>

<style lang="scss" scoped>
.sabor-fit {
  background-image: url("./assets/bg-sabor-fit.png");
  background-repeat: repeat-x;
}
</style>