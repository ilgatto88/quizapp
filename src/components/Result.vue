<template>
  <div class="results">
    <p>Your Results...</p>
    <h1>{{ numberOfCorrectAnswers }}/{{ questionLength }}</h1>
    <RouterLink to="/">Go Back</RouterLink>
  </div>
</template>

<script setup>
import { defineProps } from "vue";
import { RouterLink } from "vue-router";

const { questionLength, numberOfCorrectAnswers } = defineProps([
  "questionLength",
  "numberOfCorrectAnswers",
]);
</script>

<style scoped>
.results {
  text-align: center;
  padding: 100px 0px;
}

p {
  font-size: 25px;
}

h1 {
  font-size: 80px;
}
</style>
