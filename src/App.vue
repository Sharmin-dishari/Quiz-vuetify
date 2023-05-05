<template>
  <v-app>
    <Default-layout />
    <v-main class="bg-color">
      <router-view />
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "App",
  components: {
    DefaultLayout: () => import("./Layouts/DefaultLayout.vue"),
  },
  data: () => ({
    //
  }),
};
</script>
