<template>
  <div class="form-card text-start">
    <form>
      <div class="tab-content pt-4" id="user-detail">
        <b-col sm="12">
          <b-col md="12" class="p-0">
            <h3 class="mb-4">User Information:</h3>
            <b-row class="pb-2">
              <b-col md="6" class="form-group">
                <label class="form-label">First Name</label>
                <input
                  maxlength="100"
                  type="text"
                  required="required"
                  class="form-control"
                  placeholder="Enter First Name"
                />
              </b-col>
              <b-col md="6" class="form-group">
                <label class="form-label">Last Name</label>
                <input
                  maxlength="100"
                  type="text"
                  required="required"
                  class="form-control"
                  placeholder="Enter Last Name"
                />
              </b-col>
              <b-col md="6" class="form-group">
                <label for="uname" class="form-label">User Name: *</label>
                <input
                  type="text"
                  class="form-control"
                  id="uname"
                  required="required"
                  name="uname"
                  placeholder="Enter User Name"
                />
              </b-col>
              <b-col md="6" class="form-group">
                <label for="emailid" class="form-label">Email Id: *</label>
                <input
                  type="email"
                  id="emailid"
                  class="form-control"
                  required="required"
                  name="emailid"
                  placeholder="Email ID"
                />
              </b-col>
              <b-col md="6" class="form-group">
                <label for="pwd" class="form-label">Password: *</label>
                <input
                  type="password"
                  class="form-control"
                  required="required"
                  id="pwd"
                  name="pwd"
                  placeholder="Password"
                />
              </b-col>
              <b-col md="6" class="form-group">
                <label for="cpwd" class="form-label">Confirm Password: *</label>
                <input
                  type="password"
                  class="form-control"
                  id="cpwd"
                  required="required"
                  name="cpwd"
                  placeholder="Confirm Password"
                />
              </b-col>
              <b-col md="6" class="form-group">
                <label for="cno" class="form-label">Contact Number: *</label>
                <input
                  type="text"
                  class="form-control"
                  required="required"
                  id="cno"
                  name="cno"
                  placeholder="Contact Number"
                />
              </b-col>
              <b-col md="6" class="form-group">
                <label for="acno" class="form-label"
                  >Alternate Contact Number: *</label
                >
                <input
                  type="text"
                  class="form-control"
                  required="required"
                  id="acno"
                  name="acno"
                  placeholder="Alternate Contact Number"
                />
              </b-col>
              <b-col md="12" class="mb-3 form-group">
                <label for="address" class="form-label">Address: *</label>
                <textarea
                  name="address"
                  class="form-control"
                  id="address"
                  rows="5"
                  required="required"
                ></textarea>
              </b-col>
            </b-row>
            <button
              @click="changeTab(2)"
              class="btn btn-primary nextBtn float-end"
              type="button"
            >
              Next
            </button>
          </b-col>
        </b-col>
      </div>
    </form>
  </div>
</template>
<script>
export default {
  name: "Step1",
  methods: {
    changeTab(value) {
      this.$emit("onNext", value);
    },
  },
};
</script>
