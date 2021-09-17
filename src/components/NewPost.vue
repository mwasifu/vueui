<template>
  <div class="txtbox text-center">
    <v-form>
      <v-container>
        <v-row>
          <v-col cols="12" sm="6" md="3">
            <v-text-field label="Whats cooking?" outlined></v-text-field>
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
  padding-left: 43%;
}


</style>