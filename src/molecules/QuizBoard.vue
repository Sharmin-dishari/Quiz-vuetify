<template>
  <div class="px-2 px-md-16">
    <div v-for="(item, index) in items" :key="index" class="my-4">
      <v-list
        class="bg-white pl-2 rounded-xl"
        style="border: 1px solid #dfdfdf"
      >
        <v-row>
          <v-col sm="2" lg="2" md="2" cols="4"
            ><v-img class="imageStyle" :src="item.avatar"
          /></v-col>
          <v-col sm="10" lg="10" md="10">
            <div>
              <v-row justify="space-around">
                <v-col lg="10" md="9" sm="8">
                  <div class="pt-1">
                    <v-chip small color="#B71C1C" text-color="white">
                      DRAFT
                    </v-chip>
                  </div>
                  <div class="font-weight-bold mt-2" style="font-size: 20px">
                    Quiz title will be here
                  </div>
                  <div class="caption">
                    Lorem Ipsum is simply dummy text of the printing and
                    typesetting industry.
                  </div>
                  <div class="mt-2 mt-lg-6">
                    <div
                      align="start"
                      :class="$vuetify.breakpoint.mdAndUp && 'd-flex'"
                      style="color: grey"
                      :style="
                        $vuetify.breakpoint.mdAndDown
                          ? 'font-size: 14px'
                          : 'font-size: 16px'
                      "
                    >
                      <v-col cols="auto">
                        <div class="d-flex">
                          <div>
                            <v-icon size="22px"
                              >mdi-account-circle-outline</v-icon
                            >
                          </div>
                          <div class="ml-1" style="margin-top: 2px">
                            Andrew Smith
                          </div>
                        </div>
                      </v-col>
                      <v-col
                        cols="auto"
                        v-if="$vuetify.breakpoint.mdAndUp"
                        class="pt-md-3"
                        >|</v-col
                      >
                      <v-col cols="auto">
                        <div class="d-flex">
                          <div>
                            <v-icon size="22px"
                              >mdi-calendar-blank-outline</v-icon
                            >
                          </div>
                          <div class="ml-1">25 December, 2022</div>
                        </div>
                      </v-col>
                      <v-col
                        cols="auto"
                        v-if="$vuetify.breakpoint.mdAndUp"
                        class="pt-md-3 d-sm-none d-md-flex d-none d-sm-flex"
                        >|</v-col
                      >
                      <v-col>
                        <div class="d-flex">
                          <div>
                            <v-icon size="22px">mdi-help-circle-outline</v-icon>
                          </div>
                          <div class="ml-1" style="margin-top: 2px">
                            18 Questions
                          </div>
                        </div>
                      </v-col>
                    </div>
                  </div>
                </v-col>
                <v-col align-self="center">
                  <div>
                    <v-btn
                      tile
                      class="mr-3 py-4 rounded-pill font-weight-bold"
                      rounded
                      style="background-color: #30c7b3; color: white"
                    >
                      <v-icon left style="text-decoration: underline">
                        mdi-pencil-outline
                      </v-icon>
                      Edit
                    </v-btn>
                    <v-btn
                      small
                      fab
                      elevation="0"
                      dark
                      style="background-color: #4f92e3"
                    >
                      <v-icon dark> mdi-dots-horizontal </v-icon>
                    </v-btn>
                  </div>
                </v-col>
              </v-row>
            </div>
          </v-col>
        </v-row>
      </v-list>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    items: { type: Array, required: true },
  },
};
</script>

<style>
.caption {
  color: #6c6f85;
  font-family: Roboto;
  font-size: 16px;
  font-weight: 400;
  line-height: 22px;
  letter-spacing: 0px;
}
@media screen and (max-width: 600px) {
  .imageStyle {
    height: 103px;
    width: 120px;
    border-radius: 10px;
  }
}
</style>