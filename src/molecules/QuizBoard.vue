<template>
  <div class="px-6 px-md-16">
    <div v-for="(item, index) in items" :key="index" class="my-4">
      <v-list class="bg-white pl-2 rounded-xl border">
        <v-row>
          <v-col sm="2" lg="2" md="2" cols="4"
            ><v-img class="imageStyle" :src="item.avatar"
          /></v-col>
          <v-col sm="10" lg="10" md="10">
            <div>
              <v-row justify="space-between">
                <v-col
                  lg="10"
                  md="9"
                  sm="8"
                  :cols="$vuetify.breakpoint.smAndDown && '12'"
                >
                  <div class="pt-1">
                    <v-chip small color="#B71C1C" text-color="white">
                      DRAFT
                    </v-chip>
                  </div>
                  <div class="font-weight-bold mt-2 title-font">
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
                      :style="
                        $vuetify.breakpoint.mdAndDown
                          ? 'font-size: .9rem'
                          : 'font-size: 1rem'
                      "
                    >
                      <div class="pt-2">
                        <div class="d-flex">
                          <div>
                            <v-icon size="22px"
                              >mdi-account-circle-outline</v-icon
                            >
                          </div>
                          <div class="ml-1 info-margin">Andrew Smith</div>
                        </div>
                      </div>
                      <div v-if="$vuetify.breakpoint.mdAndUp" class="px-3 pt-2">
                        |
                      </div>
                      <div class="pt-2">
                        <div class="d-flex">
                          <div>
                            <v-icon size="22px"
                              >mdi-calendar-blank-outline</v-icon
                            >
                          </div>
                          <div class="ml-1 info-margin">25 December, 2022</div>
                        </div>
                      </div>
                      <div v-if="$vuetify.breakpoint.mdAndUp" class="px-3 pt-2">
                        |
                      </div>
                      <div class="pt-2">
                        <div class="d-flex">
                          <div>
                            <v-icon size="22px">mdi-help-circle-outline</v-icon>
                          </div>
                          <div class="ml-1 info-margin">18 Questions</div>
                        </div>
                      </div>
                    </div>
                  </div>
                </v-col>
                <v-col align-self="center">
                  <div>
                    <v-btn
                      tile
                      class="mr-3 py-4 rounded-pill font-weight-bold"
                      rounded
                      color="#30c7b3"
                      dark
                    >
                      <v-icon
                        left
                        class="text-decoration-underline"
                        color="white"
                      >
                        mdi-pencil-outline
                      </v-icon>
                      <span>Edit</span>
                    </v-btn>
                    <v-btn small fab elevation="0" dark color="#4f92e3">
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
.info-margin {
  margin-top: 2px;
  color: grey;
}
.border {
  border: 1px solid #dfdfdf;
}
.title-font {
  font-size: 1.2rem;
}
.caption {
  color: #6c6f85;
  font-family: Roboto;
  font-size: 1rem;
  font-weight: 400;
  line-height: 22px;
  letter-spacing: 0px;
}
@media screen and (max-width: 600px) {
  .imageStyle {
    height: 10vh;
    width: 12vh;
    border-radius: 10px;
  }
}
</style>