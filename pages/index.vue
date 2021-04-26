<template>
  <v-container justify-center align-center>
    <v-row>
      <v-col class="pr-0">
        <v-card class="d-flex justify-end car-box-card">
          <v-card height="50" width="19%" class="car-box ml-1 mb-1"></v-card>
          <v-card height="50" width="19%" class="car-box ml-1 mb-1"></v-card>
          <v-card height="50" width="19%" class="car-box ml-1 mb-1"></v-card>
          <v-card height="50" width="19%" class="car-box ml-1 mb-1"></v-card>
          <v-card height="50" width="19%" class="car-box ml-1 mb-1"></v-card>
        </v-card>
        <v-card class="d-flex justify-end">
          <v-card height="50" width="100%" class="car-body text-center">이사 전문</v-card>
        </v-card>
      </v-col>
      <v-col class="pl-1 mt-1">
        <v-card elevation="1" height="100" width="100" class="car-head" color="rgb(30, 30, 253)"></v-card>
      </v-col>
    </v-row>
    <v-row class="mt-0">
      <v-col>
        <v-sheet elevation="1" height="50" width="50" class="wheel"></v-sheet>
      </v-col>
      <v-col>
        <v-sheet elevation="1" height="50" width="50" class="wheel"></v-sheet>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import Bounce from 'bounce.js'

export default {
  method: {

  },
  mounted() {
    let bounce = new Bounce();
    let duration = 30;

    bounce.rotate({
      from: 0,
      to: 90,
      delay: 1,
      duration: duration
    });

    bounce.applyTo(document.querySelectorAll(".wheel"), {
      loop: true
    });
  }
}
</script>
<style scoped>
.wheel {
  border-radius: 15px 15px 15px 15px;
  color: #BDBDBD
}

.car-head {
  border-radius: 0px 40px 0px 0px;
  background-color: rgb(30, 30, 253) !important;
}

.car-body {
  background-color: rgb(30, 30, 253) !important;
}

.car-box-card {
  background-color: transparent !important;
  box-shadow: 0px 0px 0px 0px !important;
}
.car-box{
  background-color: rgba(160, 109, 52, 0.836) !important;
  border-width: 5px;
}
</style>