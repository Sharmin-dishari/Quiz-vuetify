<template>
  <v-container class="text-center">
    <v-btn color="#30c7b3" dark @click="$router.push({ name: 'quiz-board' })"
      >Start Quiz</v-btn
    >
  </v-container>
</template>

<script>
export default {
  name: "HelloWorld",

  data: () => ({}),
};
</script>
