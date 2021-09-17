<template>
  <v-container class>
    <v-row class="text-center">
      <v-col cols="12">
        <!-- <v-img
          :src="require('../assets/logo.svg')"
          class="my-3"
          contain
          height="200"
        /> -->
      </v-col>

      <v-col class="mb-4 headingsep">
        <h1 class="display-2 font-weight-bold mb-3 heading">
          Blogmeister
        </h1>

        <p class="subheading font-weight-regular firstParagraph">
          Still in the oven!
          <a class ="discord" href="https://discord.gg/QFhG6jnu"
            target="_blank"
          > Visit us on Discord!</a>
        </p>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
  export default {
    name: 'HelloWorld',

    data: () => ({
      
    }),
  }
</script>

<style scoped>

.headingsep{
  margin-top: 10%;
}

.subheading{
  color: orange;
  font-size: 1.25rem;
}
.heading{
  color: orange;
  font-size: 1.5rem;
}

.firstParagraph{
  color: orange;
}

.discord{
  color: orange;
}
</style>