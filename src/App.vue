<template>
  <v-app>
    <v-content>
      <AppBar />

      <NewPost />
    </v-content>

    <v-card height="800px">
      <v-footer v-bind="localAttrs" :padless="padless" fixed color="black">
        <v-card-text class="white--text">
          {{ new Date().getFullYear() }} — <em>Blogmeister Inc</em>
        </v-card-text>
      </v-footer>
    </v-card>
  </v-app>
</template>


// javascript


<script>

import NewPost from "./components/NewPost.vue";
import AppBar from "./components/AppBar.vue"

export default {
  components: { NewPost, AppBar},
  name: "App",

  data: () => ({
    
  }),
};
</script>


// css


<style scoped>
.toolbarBM {
  font-size: 1.65rem;
  color: orange;
  font-family: Arial, Helvetica, sans-serif;
  padding-left: 2%;
}

</style>