<template>
  <div>
    <div class="tab-content pt-4" id="document-detail">
      <b-col sm="12">
        <b-col md="12" class="p-0">
          <h3 class="mb-4">Document Details:</h3>
          <b-row>
            <b-col md="6" class="form-group">
              <label for="fname" class="form-label">Company Name: *</label>
              <input
                type="text"
                class="form-control"
                required="required"
                id="fname"
                name="fname"
                placeholder="Company Name"
              />
            </b-col>
            <b-col md="6" class="form-group">
              <div class="form-group">
                <label for="ccno" class="form-label">Contact Number: *</label>
                <input
                  type="text"
                  class="form-control"
                  required="required"
                  id="ccno"
                  name="ccno"
                  placeholder="Contact Number"
                />
              </div>
            </b-col>
            <b-col md="6" class="form-group">
              <div class="form-group">
                <label for="url" class="form-label">Company Url: *</label>
                <input
                  type="text"
                  class="form-control"
                  required="required"
                  id="url"
                  name="url"
                  placeholder="Company Url."
                />
              </div>
            </b-col>
            <b-col md="6" class="form-group">
              <div class="form-group">
                <label for="cemail" class="form-label"
                  >Company Mail Id: *</label
                >
                <input
                  type="email"
                  class="form-control"
                  required="required"
                  id="cemail"
                  name="cemail"
                  placeholder="Company Mail Id."
                />
              </div>
            </b-col>
            <b-col md="12" class="mb-2">
              <div class="form-group">
                <label for="cadd" class="form-label">Company Address: *</label>
                <textarea
                  name="cadd"
                  required="required"
                  id="cadd"
                  class="form-control"
                  rows="5"
                ></textarea>
              </div>
            </b-col>
          </b-row>
          <b-row class="justify-content-between">
            <b-col cols="auto">
              <button
                @click="changeTab(1)"
                type="button"
                class="btn btn-secondary"
                data-enchanter="previous"
              >
                Previous
              </button>
            </b-col>
            <b-col cols="auto">
              <button
                @click="changeTab(3)"
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
  name: "Step2",
  methods: {
    changeTab(value) {
      this.$emit("onNext", value);
    },
  },
};
</script>
