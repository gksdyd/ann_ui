<template>
  <div>
    <div class="tab-content pt-4 pb-2" id="cpnfirm-data">
      <b-col sm="12">
        <b-col md="12" class="p-0">
          <h3 class="mb-4 text-start">Finish:</h3>
          <b-row class="justify-content-center">
            <b-col cols="3">
              <img
                src="@/assets/images/page-img/img-success.png"
                class="img-fluid"
                alt="img-success"
              />
            </b-col>
          </b-row>
        </b-col>
        <button
        @click="changeTab(3)"
          type="button"
          class="btn btn-secondary d-none"
          data-enchanter="previous"
        >
          Previous
        </button>
        <button
          type="button"
          class="btn btn-primary float-end d-none"
          data-enchanter="finish"
        >
          Finish
        </button>
      </b-col>
    </div>
  </div>
</template>
<script>
export default {
  name: "Step3",
  methods: {
    changeTab(value) {
      this.$emit("onNext", value);
    },
  },
};
</script>