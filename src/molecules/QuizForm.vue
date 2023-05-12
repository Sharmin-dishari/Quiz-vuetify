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
               class="radio-large"
                color="#30C7B3"
                label="Public"
                value="option1"
              ></v-radio>
              <v-radio
                color="#30C7B3"
                label="Private"
                value="option2"
              ></v-radio>
            </v-radio-group>
          </v-col>
          <v-col lg="5" md="5" sm="5" cols="12" class="mx-2">
            <div
              class="font-weight-medium mb-4"
              :class="this.$vuetify.breakpoint.width < 600 && 'mt-n7'"
            >
              Quiz Image
            </div>
            <div
             :class="this.$vuetify.breakpoint.width < 600 ? 'dashed2' : 'dashed'"
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
                <img
                  class="image"
                  width="100"
                  spinner-color="white"
                  :src="url"
                  cover
                  :aspect-ratio="1"
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
      selectedSize: null,
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

.form-bg {
  background-color: white;
  border: 1px solid #dfdfdf;
}
.dashed2 {
  padding: 3vh 0;
  background-image: url("data:image/svg+xml,%3csvg width='100%25' height='100%25' xmlns='http://www.w3.org/2000/svg'%3e%3crect width='100%25' height='100%25' fill='none' rx='10' ry='10' stroke='%234F92E3FF' stroke-width='2' stroke-dasharray='6%2c 14' stroke-dashoffset='0' stroke-linecap='round'/%3e%3c/svg%3e");
}
.dashed {
  padding: 15vh 0;
  background-image: url("data:image/svg+xml,%3csvg width='100%25' height='100%25' xmlns='http://www.w3.org/2000/svg'%3e%3crect width='100%25' height='100%25' fill='none' rx='10' ry='10' stroke='%234F92E3FF' stroke-width='2' stroke-dasharray='6%2c 14' stroke-dashoffset='0' stroke-linecap='round'/%3e%3c/svg%3e");



  
}


</style>