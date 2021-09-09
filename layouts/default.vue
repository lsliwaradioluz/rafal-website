<template>
  <v-app>
    <app-header />
    <!-- Sizes your content based upon application components -->
    <v-main>
      <!-- Provides the application the proper gutter -->
      <v-container fluid>

        <!-- If using vue-router -->
        <router-view></router-view>
      </v-container>
    </v-main>

    <v-footer app>
      <!-- -->
    </v-footer>
  </v-app>
</template>

<script>
import AppHeader from '~/components/AppHeader.vue';
export default {
  components: { AppHeader }
}
</script>

<style>

</style>