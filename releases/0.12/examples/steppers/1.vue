<template>
  <v-stepper v-model="e1">
    <v-stepper-header>
      <v-stepper-step step="1" :complete="e1 > 1">Name of step 1</v-stepper-step>
      <v-divider></v-divider>
      <v-stepper-step step="2" :complete="e1 > 2">Name of step 2</v-stepper-step>
      <v-divider></v-divider>
      <v-stepper-step step="3">Name of step 3</v-stepper-step>
    </v-stepper-header>
    <v-stepper-content step="1">
      <v-card class="grey lighten-1 z-depth-1 mb-5" height="200px"></v-card>
      <v-btn primary @click.native="e1 = 2" light>Continue</v-btn>
      <v-btn flat dark>Cancel</v-btn>
    </v-stepper-content>
    <v-stepper-content step="2">
      <v-card class="grey lighten-1 z-depth-1 mb-5" height="200px"></v-card>
      <v-btn primary @click.native="e1 = 3" light>Continue</v-btn>
      <v-btn flat dark>Cancel</v-btn>
    </v-stepper-content>
    <v-stepper-content step="3">
      <v-card class="grey lighten-1 z-depth-1 mb-5" height="200px"></v-card>
      <v-btn primary @click.native="e1 = 1" light>Continue</v-btn>
      <v-btn flat dark>Cancel</v-btn>
    </v-stepper-content>
  </v-stepper>
</template>

<script>
  export default {
    data () {
      return {
        e1: 0
      }
    }
  }
</script>
