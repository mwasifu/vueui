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
      <v-btn elevation="0" icon @click.stop="drawer = !drawer">
        <v-app-bar-nav-icon></v-app-bar-nav-icon>
      </v-btn>

      <v-navigation-drawer v-model="drawer" absolute temporary>
        <v-list-item>
          <v-list-item-avatar>
            <v-img src="https://randomuser.me/api/portraits/men/78.jpg"></v-img>
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

      <v-spacer></v-spacer>
      <v-toolbar-title class="text-uppercase toolbarBM">
        <span class="font-weight-light">Blog</span>
        <span class="font-weight-bold">meister</span>
      </v-toolbar-title>

      <v-spacer></v-spacer>
      <v-checkbox
        v-model="collapseOnScroll"
        color="white"
        hide-details
      ></v-checkbox>

      <v-toolbar-items class="hidden-sm-and-down">
        <v-btn elevation="0" color="orange">Login</v-btn>
      </v-toolbar-items>
    </v-app-bar>
    <v-sheet
      id="scrolling-techniques-6"
      class="overflow-y-auto"
      max-height="600"
    >
      <v-container style="height: 60px"></v-container>
    </v-sheet>
  </div>
</template>

<script>
export default {
  name: "AppBar",
  data: () => ({
    collapseOnScroll: true,

    return: {
      drawer: null,
      items: [
        { title: 'Home', icon: 'mdi-view-dashboard' },
        { title: 'About', icon: 'mdi-forum' },
      ],
    }
  }),
};
</script>