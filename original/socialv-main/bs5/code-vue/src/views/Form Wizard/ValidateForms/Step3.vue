<template>
  <div>
    <div class="tab-content pt-4" id="bank-detail">
      <b-col sm="12">
        <b-col md="12" class="p-0">
          <h3 class="mb-4">Bank Detail:</h3>
          <b-row class="pb-2">
            <b-col md="6" class="form-group">
              <label for="panno" class="form-label">Pan No: *</label>
              <input
                type="text"
                class="form-control"
                required="required"
                id="panno"
                name="panno"
                placeholder="Pan No."
              />
            </b-col>
            <b-col md="6" class="form-group">
              <label for="accno" class="form-label">Account No: *</label>
              <input
                type="text"
                class="form-control"
                required="required"
                id="accno"
                name="accno"
                placeholder="Account No."
              />
            </b-col>
            <b-col md="6" class="form-group">
              <label for="accname" class="form-label"
                >Account Holder Name: *</label
              >
              <input
                type="text"
                class="form-control"
                required="required"
                id="accname"
                name="accname"
                placeholder="Account Holder Name."
              />
            </b-col>
            <b-col md="6" class="form-group">
              <label for="ifsc" class="form-label">IFSC Code: *</label>
              <input
                type="text"
                class="form-control"
                required="required"
                id="ifsc"
                name="ifsc"
                placeholder="IFSC Code."
              />
            </b-col>
            <b-col md="6" class="form-group">
              <label for="bankname" class="form-label">Bank Name: *</label>
              <input
                type="text"
                class="form-control"
                required="required"
                id="bankname"
                name="bankname"
                placeholder="Bank Name."
              />
            </b-col>
            <b-col md="6" class="form-group">
              <label for="branch" class="form-label">Bank Branch Name: *</label>
              <input
                type="text"
                class="form-control"
                required="required"
                id="branch"
                name="branch"
                placeholder="Bank Branch Name."
              />
            </b-col>
          </b-row>
          <b-row class="justify-content-between">
            <b-col cols="auto">
              <button
                @click="changeTab(2)"
                type="button"
                class="btn btn-secondary"
                data-enchanter="previous"
              >
                Previous
              </button>
            </b-col>
            <b-col cols="auto">
              <button
                @click="changeTab(4)"
                class="btn btn-primary nextBtn float-end"
                type="button"
              >
                Next
              </button>
            </b-col>
          </b-row>
        </b-col>
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
