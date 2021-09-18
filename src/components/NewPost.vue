<template>
  <div class="txtbox text-center">
    <v-form>
      <v-container>
        <v-row>
          <v-col cols="12" lg="12" sm="12" md="12">
            <v-text-field label="Whats cooking?" outlined color="orange"></v-text-field>
            <div class="text-center">
            <v-btn rounded color="orange" dark> + New Post </v-btn>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </v-form>
  </div>
</template>

<script>
export default {
  name: "NewPost",
};
</script>

<style scoped>
.txtbox {
  justify-content: center;
  margin: 0 25% 0 25%;
}


</style>