<template>
  <div>
    <div class="mx-md-10 mx-5 my-4 form-bg rounded-lg">
      <form>
        <v-row justify="space-around" class="mx-1 my-2">
          <v-col lg="5" md="5" sm="5" cols="12">
            <div class="font-weight-medium mb-2">Quiz Title</div>
            <v-text-field
              label="Enter Quiz title"
              class="rounded-pill"
              outlined
              v-model="quiz_title"
            ></v-text-field>
            <div class="font-weight-medium mb-2">Description</div>
            <v-textarea
              outlined
              name="input-7-4"
              class="rounded-lg"
              label="Enter Description"
              v-model="quiz_description"
            ></v-textarea>
            <div class="font-weight-medium">Quiz Type</div>
            <v-radio-group v-model="quiz_type" row>
              <v-radio
                color="#30C7B3"
                label="Option 1"
                value="option1"
              ></v-radio>
              <v-radio
                color="#30C7B3"
                label="Option 2"
                value="option2"
              ></v-radio>
            </v-radio-group>
          </v-col>
          <v-col lg="5" md="5" sm="5" cols="12">
            <div
              class="font-weight-medium mb-4"
              :class="this.$vuetify.breakpoint.width < 600 && 'mt-n7'"
            >
              Quiz Image
            </div>
            <div
              :class="
                this.$vuetify.breakpoint.width < 600 ? 'dashed2' : 'dashed'
              "
              align="center"
            >
              <label for="file-btn" class="upload" style="cursor: pointer">
                <input
                  type="file"
                  id="file-btn"
                  ref="fileUrl"
                  @change="handleFileUpload"
                  hidden
                />
                <!-- <v-icon left color="blue" class="text-center" size="70px">
                  mdi-image-outline
                </v-icon> -->
                <v-img
                  class="image"
                  spinner-color="white"
                  :src="url"
                  style="width: 80px"
                />
                <div class="font-weight-medium">Upload Image</div>
                <div class="text-caption text-center">
                  Or Drag & Drop Image file here
                </div>
              </label>
            </div>
          </v-col>
        </v-row>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      quiz_title: "",
      quiz_description: "",
      url: "/gallary.png",
      quiz_type: "option1",
    };
  },
  methods: {
    async handleFileUpload(event) {
      this.file = event.target.files[0];
      this.url = URL.createObjectURL(this.file);
    },
  },
};
</script>

<style>
.border {
  border: 1px solid #dfdfdf;
}
.form-bg {
  background-color: white;
  border: 1px solid #dfdfdf;
}
.dashed2 {
  border-style: dashed;
  border-radius: 10px;
  padding: 30px 0;
}
.dashed {
  border-style: dashed;
  border-radius: 10px;
  padding: 120px 0;
}
</style>