<template>
  <v-container>
    <v-app-bar app color="white">
      <div class="d-flex align-center">
        <v-btn target="_blank" text v-if="$vuetify.breakpoint.mdAndUp">
          <v-icon>mdi-heart-outline</v-icon>
        </v-btn>

        <v-btn target="_blank" text>
          <v-icon>mdi-message-outline</v-icon>
        </v-btn>
        <v-btn target="_blank" text>
          <v-icon>mdi-email-outline</v-icon>
        </v-btn>
        <v-badge dot color="green" class="mx-4">
          <v-icon> mdi-bell-outline </v-icon>
        </v-badge>

        <v-btn target="_blank" text v-if="$vuetify.breakpoint.mdAndUp">
          <v-icon>mdi-dots-grid</v-icon>
        </v-btn>
      </div>

      <v-spacer></v-spacer>
      <v-spacer></v-spacer>

      <v-text-field
        outlined
        v-if="$vuetify.breakpoint.mdAndUp"
        class="mt-6"
        style="border-radius: 50px; width: 70px"
        dense
        label="Search"
        prepend-inner-icon="mdi-magnify"
      ></v-text-field>
      <v-btn target="_blank" text v-else class="mr-n6">
        <v-icon>mdi-magnify</v-icon>
      </v-btn>
      <v-badge dot color="green" class="ml-6">
        <v-icon> mdi-cart-outline </v-icon>
      </v-badge>

      <v-avatar size="36" class="ml-6">
        <img src="https://cdn.vuetifyjs.com/images/john.jpg" alt="John" />
      </v-avatar>
    </v-app-bar>
  </v-container>
</template>

<script>
export default {};
</script>

<style>
</style>