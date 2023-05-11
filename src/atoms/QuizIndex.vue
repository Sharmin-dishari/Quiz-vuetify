<template>
  <div class="py-6">
    <v-row justify="space-between" class="px-md-16 px-5">
      <v-col>
        <div class="pa-2 ma-2 font-weight-bold text-h5">Quiz List</div>
      </v-col>
      <v-col align="end">
        <v-btn
          v-if="$vuetify.breakpoint.smAndUp"
          tile
          class="mr-3 py-6 rounded-pill font-weight-bold"
          rounded
          to="/create-quiz"
          dark
          color="#182e46"
        >
          <v-icon left size="27px"> mdi-plus </v-icon>
          Create Quiz
        </v-btn>
        <v-btn
          v-else
          color="#182e46"
          dark
          class="mt-3 mx-2"
          to="/create-quiz"
          fab
          small
        >
          <v-icon size="30px"> mdi-plus </v-icon>
        </v-btn>
      </v-col>
    </v-row>
    <QuizBoard :items="itemList" />
  </div>
</template>

<script>
import QuizBoard from "@/molecules/QuizBoard.vue";
export default {
  components: { QuizBoard },
  data: () => ({
    itemList: [
      {
        active: true,
        avatar: "/image1.png",
        title: "Jason Oner",
      },
      {
        active: true,
        avatar: "/image2.png",
        title: "Mike Carlson",
      },
      {
        avatar: "/image3.png",
        title: "Cindy Baker",
      },
      {
        avatar: "/image4.png",
        title: "Ali Connors",
      },
    ],
  }),
};
</script>
