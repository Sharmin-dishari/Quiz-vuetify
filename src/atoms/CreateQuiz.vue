<template>
  <div class="py-6 mb-10">
    <v-row justify="space-between" class="px-md-16 px-4">
      <v-col>
        <div class="ma-2 font-weight-bold text-h5">Create Quiz</div>
      </v-col>
      <v-col align="end">
        <v-btn
          tile
          dark
          large
          to="/quiz-board"
          class="rounded-pill"
          color="#A1A1A1"
          v-if="$vuetify.breakpoint.smAndUp"
        >
          <v-icon left> mdi-arrow-left </v-icon>
          Back
        </v-btn>
        <v-btn
          large
          v-if="$vuetify.breakpoint.smAndUp"
          color="#182e46"
          class="ma-2 white--text rounded-pill"
        >
          Next
          <v-icon right dark> mdi-arrow-right </v-icon>
        </v-btn>
        <div v-else>
          <v-btn
            color="#A1A1A1"
            dark
            class="mt-3 mx-2"
            fab
            x-small
            to="/quiz-board"
          >
            <v-icon size="30px"> mdi-arrow-left </v-icon>
          </v-btn>
          <v-btn color="#182e46" dark class="mt-3" fab x-small>
            <v-icon size="30px"> mdi-arrow-right </v-icon>
          </v-btn>
        </div>
      </v-col>
    </v-row>
    <QuizForm class="pb-10" />
    <!-- <v-fab-transition>
      <v-btn v-show="!hidden" color="pink" dark absolute top right fab>
        <v-icon>mdi-plus</v-icon>
      </v-btn>
    </v-fab-transition> -->
    <v-row justify="space-between" class="px-md-16 px-5">
      <v-col v-if="$vuetify.breakpoint.smAndUp"> </v-col>
      <v-col
        class="fixedButton pt-10"
        :align="$vuetify.breakpoint.smAndUp ? 'end' : 'center'"
      >
        <v-btn
          large
          tile
          dark
          class="rounded-pill"
          color="#A1A1A1"
          to="/quiz-board"
        >
          <v-icon left> mdi-arrow-left </v-icon>
          Back
        </v-btn>
        <v-btn large color="#182e46" class="ma-2 white--text rounded-pill">
          Next
          <v-icon right dark> mdi-arrow-right </v-icon>
        </v-btn>
      </v-col>
    </v-row>
  </div>
</template>

<script>
import QuizForm from "@/molecules/QuizForm.vue";
export default {
  components: { QuizForm },
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
<style>
.fixedButton {
  bottom: 1rem;
  right: 2rem;
}

@media only screen and (max-width: 600px) {
  .fixedButton {
    margin-top: 10vh;
    bottom: 0.5rem;
    right: 0;
  }
}
</style>
