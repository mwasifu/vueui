<template>
  <v-app>
    <v-content>
      <AppBar />

       <v-container class="heading-container">
        <v-row class="text-center">
          <v-col class="mb-4 headingsep">
            <span class="display-2 font-weight-light mb-3 heading blog"
              >Blog</span
            >
            <span class="display-2 font-weight-medium mb-3 heading meister"
              >meister</span
            >

            <p class="subheading font-weight-regular firstParagraph">
              Still in the oven!
              <a
                class="discord"
                href="https://discord.gg/QFhG6jnu"
                target="_blank"
              >
                Visit us on Discord!</a
              >
            </p>
          </v-col>
        </v-row>
      </v-container>




      <NewPost />
    </v-content>

    <v-card height="800px">
      <v-footer v-bind="localAttrs" :padless="padless" fixed color="black">
        <v-card-text class="white--text footer-info">
          {{ new Date().getFullYear() }} — <em>Blogmeister Inc</em>
        </v-card-text>
      </v-footer>
    </v-card>
  </v-app>
</template>




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




<style scoped>
.toolbarBM {
  font-size: 1.65rem;
  color: orange;
  font-family: Arial, Helvetica, sans-serif;
  padding-left: 2%;
}

.footer-info{
  text-align: center;
}

.heading-container{
  justify-content: center;
  position: relative;
  padding-top: 15%;
}

.discord {
  color: orange;
}

.blog {
  color: orange;
}


</style>