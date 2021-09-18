<template>
  <div>
    <v-app-bar
      :collapse="!collapseOnScroll"
      :collapse-on-scroll="collapseOnScroll"
      fixed
      color="charcoal"
      dark
      scroll-target="#scrolling-techniques-6"
    >
      <!-- <v-card class="overflow-hidden">
        <v-sheet
          height="800"
          class="overflow-hidden"
          style="position: relative"
        >
          <v-container class="fill-height"> -->
            <v-btn @click="drawer != drawer">+</v-btn>

            <v-navigation-drawer app v-model="drawer" absolute temporary>
              <v-list-item>
                <v-list-item-avatar>
                  <v-img
                    src="https://randomuser.me/api/portraits/men/78.jpg"
                  ></v-img>
                </v-list-item-avatar>

                <v-list-item-content>
                  <v-list-item-title>John Leider</v-list-item-title>
                </v-list-item-content>
              </v-list-item>

              <v-divider></v-divider>

              <v-list dense>
                <v-list-item v-for="item in items" :key="item.title" link>
                  <v-list-item-icon>
                    <v-icon>{{ item.icon }}</v-icon>
                  </v-list-item-icon>

                  <v-list-item-content>
                    <v-list-item-title>{{ item.title }}</v-list-item-title>
                  </v-list-item-content>
                </v-list-item>
              </v-list>
            </v-navigation-drawer>
          <!-- </v-container>
        </v-sheet>
      </v-card> -->

      <v-spacer></v-spacer>
      <v-toolbar-title class="text-uppercase toolbarBM">
        <span class="font-weight-light blog">Blog</span>
        <span class="font-weight-bold">meister</span>
      </v-toolbar-title>

      <v-spacer></v-spacer>

      <v-toolbar-items class="hidden-sm-and-down">
        <v-btn elevation="0" color="orange">Login</v-btn>
      </v-toolbar-items>
    </v-app-bar>

    <v-sheet
      id="scrolling-techniques-6"
      class="overflow-y-auto"
      max-height="600"
    >
      <v-container style="height: 1000px"></v-container>
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
    </v-sheet>
  </div>
</template>

<script>
export default {
  name: "AppBar",
  data: () => ({
    collapseOnScroll: true,

    return: {
      drawer: true,
      items: [
        { title: "Home", icon: "mdi-view-dashboard" },
        { title: "About", icon: "mdi-forum" },
      ],
    },
  }),
};
</script>

<style scoped>
.headingsep {
  margin-top: 12%;
}

.heading {
  color: #212121;
  font-size: 1.5rem;
}

.firstParagraph {
  margin-top: 1%;
  color: #212121;
}

.discord {
  color: orange;
}

.blog {
  color: orange;
}

.heading-container{
  justify-content: center;
  position: absolute;
  bottom: 50%;
}
</style> 