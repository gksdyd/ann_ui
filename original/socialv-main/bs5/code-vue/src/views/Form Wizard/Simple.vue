<template>
  <div class="content-inner">
    <b-container>
      <b-row>
        <b-col sm="12">
          <div class="card position-relative inner-page-bg bg-primary" style="height: 150px">
            <div class="inner-page-title">
              <h3 class="text-white">Simple Wizard Page</h3>
              <p class="text-white">lorem ipsum</p>
            </div>
          </div>
        </b-col>
        <b-col sm="12" lg="12">
          <iq-card>
            <template v-slot:headerTitle>
              <h4 class="card-title">Simple Wizard</h4>
            </template>
            <b-card-body class="pt-0">
              <form id="form-wizard1" class="text-center mt-0">
                <ul id="top-tab-list" class="p-0 row list-inline">
                  <li :class="checkActive(0, 1)" class="col-lg-3 col-md-6 mb-2 text-start active" id="account">
                    <a href="javascript:void(0);">
                      <i class="material-symbols-outlined">lock_open</i><span>Account</span>
                    </a>
                  </li>
                  <li :class="checkActive(1, 2)" class="col-lg-3 col-md-6 mb-2 text-start" id="personal">
                    <a href="javascript:void(0);">
                      <i class="material-symbols-outlined">person</i><span>Personal</span>
                    </a>
                  </li>
                  <li :class="checkActive(2, 3)" class="col-lg-3 col-md-6 mb-2 text-start" id="payment">
                    <a href="javascript:void(0);">
                      <i class="material-symbols-outlined">photo_camera</i><span>Image</span>
                    </a>
                  </li>
                  <li :class="checkActive(3, 4)" class="col-lg-3 col-md-6 mb-2 text-start" id="confirm">
                    <a href="javascript:void(0);">
                      <i class="material-symbols-outlined">done</i><span>Finish</span>
                    </a>
                  </li>
                </ul>
                <!-- fieldsets -->
                <fieldset :class="current == 1 ? 'd-block' : 'd-none'">
                  <div class="form-card text-start">
                    <div class="row">
                      <div class="col-7">
                        <h3 class="mb-4">Account Information:</h3>
                      </div>
                      <div class="col-5">
                        <h2 class="steps">Step 1 - 4</h2>
                      </div>
                    </div>
                    <div class="row">
                      <div class="col-md-6">
                        <div class="form-group">
                          <label class="form-label">Email: *</label>
                          <input type="email" class="form-control" name="email" placeholder="Email Id" />
                        </div>
                      </div>
                      <div class="col-md-6">
                        <div class="form-group">
                          <label class="form-label">Username: *</label>
                          <input type="text" class="form-control" name="uname" placeholder="UserName" />
                        </div>
                      </div>
                      <div class="col-md-6">
                        <div class="form-group">
                          <label class="form-label">Password: *</label>
                          <input type="password" class="form-control" name="pwd" placeholder="Password" />
                        </div>
                      </div>
                      <div class="col-md-6">
                        <div class="form-group">
                          <label class="form-label">Confirm Password: *</label>
                          <input type="password" class="form-control" name="cpwd" placeholder="Confirm Password" />
                        </div>
                      </div>
                    </div>
                  </div>
                  <button type="button" name="next" @click="changeTab(2)"
                    class="btn btn-primary next action-button float-end" value="Next">
                    Next
                  </button>
                </fieldset>
                <fieldset :class="current == 2 ? 'd-block' : 'd-none'">
                  <div class="form-card text-start">
                    <div class="row">
                      <div class="col-7">
                        <h3 class="mb-4">Personal Information:</h3>
                      </div>
                      <div class="col-5">
                        <h2 class="steps">Step 2 - 4</h2>
                      </div>
                    </div>
                    <div class="row">
                      <div class="col-md-6">
                        <div class="form-group">
                          <label class="form-label">First Name: *</label>
                          <input type="text" class="form-control" name="fname" placeholder="First Name" />
                        </div>
                      </div>
                      <div class="col-md-6">
                        <div class="form-group">
                          <label class="form-label">Last Name: *</label>
                          <input type="text" class="form-control" name="lname" placeholder="Last Name" />
                        </div>
                      </div>
                      <div class="col-md-6">
                        <div class="form-group">
                          <label class="form-label">Contact No.: *</label>
                          <input type="text" class="form-control" name="phno" placeholder="Contact No." />
                        </div>
                      </div>
                      <div class="col-md-6">
                        <div class="form-group">
                          <label class="form-label">Alternate Contact No.: *</label>
                          <input type="text" class="form-control" name="phno_2" placeholder="Alternate Contact No." />
                        </div>
                      </div>
                    </div>
                  </div>
                  <button type="button" name="next" @click="changeTab(3)"
                    class="btn btn-primary next action-button float-end" value="Next">
                    Next
                  </button>
                  <button type="button" name="previous" @click="changeTab(1)"
                    class="btn btn-dark previous action-button-previous float-end me-3" value="Previous">
                    Previous
                  </button>
                </fieldset>
                <fieldset :class="current == 3 ? 'd-block' : 'd-none'">
                  <div class="form-card text-start">
                    <div class="row">
                      <div class="col-7">
                        <h3 class="mb-4">Image Upload:</h3>
                      </div>
                      <div class="col-5">
                        <h2 class="steps">Step 3 - 4</h2>
                      </div>
                    </div>
                    <div class="form-group">
                      <label class="form-label">Upload Your Photo:</label>
                      <input type="file" class="form-control" name="pic" accept="image/*" />
                    </div>
                    <div class="form-group">
                      <label class="form-label">Upload Signature Photo:</label>
                      <input type="file" class="form-control" name="pic-2" accept="image/*" />
                    </div>
                  </div>
                  <button type="button" name="next" @click="changeTab(4)"
                    class="btn btn-primary next action-button float-end" value="Submit">
                    Submit
                  </button>
                  <button type="button" name="previous" @click="changeTab(2)"
                    class="btn btn-dark previous action-button-previous float-end me-3" value="Previous">
                    Previous
                  </button>
                </fieldset>
                <fieldset :class="current == 4 ? 'd-block' : 'd-none'">
                  <div class="form-card">
                    <div class="row">
                      <div class="col-7">
                        <h3 class="mb-4 text-start">Finish:</h3>
                      </div>
                      <div class="col-5">
                        <h2 class="steps">Step 4 - 4</h2>
                      </div>
                    </div>
                    <br /><br />
                    <h2 class="text-success text-center">
                      <strong>SUCCESS !</strong>
                    </h2>
                    <br />
                    <div class="row justify-content-center">
                      <div class="col-3">
                        <img src="@/assets/images/page-img/img-success.png" class="img-fluid" alt="fit-image" />
                      </div>
                    </div>
                    <br /><br />
                    <div class="row justify-content-center">
                      <div class="col-7 text-center">
                        <h5 class="purple-text text-center">
                          You Have Successfully Signed Up
                        </h5>
                      </div>
                    </div>
                  </div>
                </fieldset>
              </form>
            </b-card-body>
          </iq-card>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>
<script>
export default {
  name: "Simple",
  data() {
    return {
      current: 1,
    };
  },
  methods: {
    changeTab(tab) {
      this.current = tab;
      window.scrollTo({ top: 0, behavior: "smooth" });
    },
    checkActive(item, active) {
      let className = "";
      if (this.current > item) {
        className = "active";
      }
      if (this.current > active) {
        className = className + " done";
      }
      return className;
    },
  },
};
</script>
