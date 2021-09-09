<template>
  <v-app-bar
    app
    color="white"
    dense
    dark
  >
    <v-img
      max-height="40"
      max-width="40"
      :src="require('~/static/logo.jpg')"
    />

    <v-tabs class="d-none d-sm-flex">
      <v-tab class="purple--text">Link 1</v-tab>
      <v-tab class="purple--text">Link 2</v-tab>
      <v-tab class="purple--text">Link 3</v-tab>
    </v-tabs>

    <v-spacer />

    <v-app-bar-nav-icon
      class="purple--text d-flex d-sm-none"
      @click="toggleMobileMenu"
    />
    <v-navigation-drawer
      app
      temporary
      right
      absolute
      color="white"
      v-model="showMobileMenu"
    >
      <v-list>
        <v-list-item
          link
        >
          <v-list-item-content>
            <v-list-item-title class="purple--text">Link 1</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item
          link
        >
          <v-list-item-content>
            <v-list-item-title class="purple--text">Link 2</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item
          link
        >
          <v-list-item-content>
            <v-list-item-title class="purple--text">Link 3</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <!-- <v-menu
      left
      bottom
    >
      <template v-slot:activator="{ on, attrs }">
        <v-btn
          icon
          v-bind="attrs"
          v-on="on"
        >
          <v-icon>mdi-dots-vertical</v-icon>
        </v-btn>
      </template>

      <v-list>
        <v-list-item
          v-for="n in 5"
          :key="n"
          @click="() => {}"
        >
          <v-list-item-title>Option {{ n }}</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-menu> -->
  </v-app-bar>
</template>

<script>
export default {
  data () {
    return {
      showMobileMenu: false
    }
  },
  methods: {
    toggleMobileMenu () {
      this.showMobileMenu = !this.showMobileMenu;
    }
  }
}
</script>

<style>

</style>