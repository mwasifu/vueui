<template>
  <v-app>
    <v-content>
      <AppBar />
      <HelloWorld />
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
import HelloWorld from "./components/HelloWorld.vue";
import NewPost from "./components/NewPost.vue";
import AppBar from "./components/AppBar.vue"

export default {
  components: { HelloWorld, NewPost, AppBar},
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