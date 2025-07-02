<template>
  <div class="content-inner">
    <b-container>
      <b-row>
        <b-col sm="12">
          <b-card no-body class="position-relative inner-page-bg bg-primary" style="height: 150px">
            <div class="inner-page-title">
              <h3 class="text-white">Validation Form Page</h3>
              <p class="text-white">lorem ipsum</p>
            </div>
          </b-card>
        </b-col>
        <b-col sm="12" lg="6">
          <iq-card>
            <template v-slot:headerTitle>
              <h4 class="card-title">Default Validation</h4>
            </template>
            <b-card-body class="pt-0">
              <p>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi
                vulputate, ex ac venenatis mollis, diam nibh finibus leo
              </p>
              <form action="#">
                <b-row>
                  <b-col md="6" class="mb-3">
                    <label class="form-label" for="validationDefault01">First name</label>
                    <input type="text" class="form-control" id="validationDefault01" required />
                  </b-col>
                  <b-col md="6" class="mb-3">
                    <label class="form-label" for="validationDefault02">Last name</label>
                    <input type="text" class="form-control" id="validationDefault02" required />
                  </b-col>
                  <b-col md="6" class="mb-3">
                    <label class="form-label" for="validationDefaultUsername">Username</label>
                    <div class="input-group">
                      <div class="input-group-prepend">
                        <span class="input-group-text" id="inputGroupPrepend2">@</span>
                      </div>
                      <input type="text" class="form-control" id="validationDefaultUsername"
                        aria-describedby="inputGroupPrepend2" required />
                    </div>
                  </b-col>
                  <b-col md="6" class="mb-3">
                    <label class="form-label" for="validationDefault03">City</label>
                    <input type="text" class="form-control" id="validationDefault03" required />
                  </b-col>
                  <b-col md="6" class="mb-3">
                    <label class="form-label" for="validationDefault04">State</label>
                    <select class="form-select" id="validationDefault04" required>
                      <option selected disabled value="">Choose...</option>
                      <option>...</option>
                    </select>
                  </b-col>
                  <b-col md="6" class="mb-3">
                    <label class="form-label" for="validationDefault05">Zip</label>
                    <input type="text" class="form-control" id="validationDefault05" required />
                  </b-col>
                </b-row>
                <div class="form-group">
                  <div class="form-check">
                    <input class="form-check-input" type="checkbox" value="" id="invalidCheck2" required />
                    <label class="form-check-label" for="invalidCheck2">
                      Agree to terms and conditions
                    </label>
                  </div>
                </div>
                <div class="form-group mb-0">
                  <button class="btn btn-primary" type="submit">
                    Submit form
                  </button>
                </div>
              </form>
            </b-card-body>
          </iq-card>
          <iq-card>
            <template v-slot:headerTitle>
              <h4 class="card-title">Supported elements</h4>
            </template>
            <b-card-body class="pt-0">
              <p>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi
                vulputate, ex ac venenatis mollis, diam nibh finibus leo
              </p>
              <form class="was-validated" action="#">
                <div class="form-group">
                  <label for="validationTextarea" class="form-label">Textarea</label>
                  <textarea class="form-control is-invalid" id="validationTextarea"
                    placeholder="Required example textarea" required></textarea>
                  <div class="invalid-feedback">
                    Please enter a message in the textarea.
                  </div>
                </div>
                <div class="form-check form-group">
                  <input type="checkbox" class="form-check-input" id="validationFormCheck1" required />
                  <label class="form-check-label" for="validationFormCheck1">Check this checkbox</label>
                  <div class="invalid-feedback">
                    Example invalid feedback text
                  </div>
                </div>
                <div class="form-check form-group me-2">
                  <input type="radio" class="form-check-input" id="validationFormCheck2" name="radio-stacked"
                    required />
                  <label class="form-check-label" for="validationFormCheck2">Toggle this radio</label>
                </div>
                <div class="form-check form-group">
                  <input type="radio" class="form-check-input" id="validationFormCheck3" name="radio-stacked"
                    required />
                  <label class="form-check-label" for="validationFormCheck3">Or toggle this other radio</label>
                  <div class="invalid-feedback">
                    More example invalid feedback text
                  </div>
                </div>
                <div class="form-group">
                  <select class="form-select" required>
                    <option value="">Open this select menu</option>
                    <option value="1">One</option>
                    <option value="2">Two</option>
                    <option value="3">Three</option>
                  </select>
                  <div class="invalid-feedback">
                    Example invalid select feedback
                  </div>
                </div>
                <div class="form-group mb-0">
                  <input type="file" class="form-control" id="validatedCustomFile" required />
                  <div class="invalid-feedback">
                    Example invalid form file feedback
                  </div>
                </div>
              </form>
            </b-card-body>
          </iq-card>
        </b-col>
        <b-col sm="12" lg="6">
          <iq-card>
            <template v-slot:headerTitle>
              <h4 class="card-title">Custom Validation</h4>
            </template>
            <b-card-body class="pt-0">
              <p>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi
                vulputate, ex ac venenatis mollis, diam nibh finibus leo
              </p>
              <form class="row g-3 needs-validation" novalidate action="#">
                <b-col md="6">
                  <label class="form-label" for="validationCustom01">First name</label>
                  <input type="text" class="form-control" id="validationCustom01" required />
                  <div class="valid-feedback">Looks good!</div>
                </b-col>
                <b-col md="6">
                  <label class="form-label" for="validationCustom02">Last name</label>
                  <input type="text" class="form-control" id="validationCustom02" required />
                  <div class="valid-feedback">Looks good!</div>
                </b-col>
                <b-col md="6">
                  <label class="form-label" for="validationCustomUsername">Username</label>
                  <div class="input-group">
                    <span class="input-group-text" id="inputGroupPrepend">@</span>
                    <input type="text" class="form-control" id="validationCustomUsername"
                      aria-describedby="inputGroupPrepend" required />
                    <div class="invalid-feedback">
                      Please choose a username.
                    </div>
                  </div>
                </b-col>
                <b-col md="6">
                  <label class="form-label" for="validationCustom03">City</label>
                  <input type="text" class="form-control" id="validationCustom03" required />
                  <div class="invalid-feedback">
                    Please provide a valid city.
                  </div>
                </b-col>
                <b-col md="6">
                  <label class="form-label" for="validationDefault04">State</label>
                  <select class="form-select" id="validationDefault04" required>
                    <option selected disabled value="">Choose...</option>
                    <option>...</option>
                  </select>
                </b-col>
                <b-col md="6">
                  <label class="form-label" for="validationCustom05">Zip</label>
                  <input type="text" class="form-control" id="validationCustom05" required />
                  <div class="invalid-feedback">
                    Please provide a valid zip.
                  </div>
                </b-col>
                <b-col cols="12">
                  <div class="form-check">
                    <input class="form-check-input" type="checkbox" value="" id="invalidCheck" required />
                    <label class="form-check-label" for="invalidCheck">
                      Agree to terms and conditions
                    </label>
                    <div class="invalid-feedback">
                      You must agree before submitting.
                    </div>
                  </div>
                </b-col>
                <b-col cols="12">
                  <button class="btn btn-primary" type="submit">
                    Submit form
                  </button>
                </b-col>
              </form>
            </b-card-body>
          </iq-card>
          <iq-card>
            <template v-slot:headerTitle>
              <h4 class="card-title">Tooltips</h4>
            </template>
            <b-card-body class="pt-0">
              <p>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi
                vulputate, ex ac venenatis mollis, diam nibh finibus leo
              </p>
              <form class="needs-validation" novalidate action="#">
                <b-row>
                  <b-col md="6" class="mb-3">
                    <label class="form-label" for="validationTooltip01">First name</label>
                    <input type="text" class="form-control" id="validationTooltip01" value="Mark" required />
                    <div class="valid-tooltip">Looks good!</div>
                  </b-col>
                  <b-col md="6" class="mb-3">
                    <label class="form-label" for="validationTooltip02">Last name</label>
                    <input type="text" class="form-control" id="validationTooltip02" value="Otto" required />
                    <div class="valid-tooltip">Looks good!</div>
                  </b-col>
                  <b-col md="6" class="mb-3">
                    <label class="form-label" for="validationTooltipUsername">Username</label>
                    <div class="input-group">
                      <div class="input-group-prepend">
                        <span class="input-group-text" id="validationTooltipUsernamePrepend">@</span>
                      </div>
                      <input type="text" class="form-control" id="validationTooltipUsername"
                        aria-describedby="validationTooltipUsernamePrepend" required />
                      <div class="invalid-tooltip">
                        Please choose a unique and valid username.
                      </div>
                    </div>
                  </b-col>
                  <b-col md="6" class="mb-3">
                    <label class="form-label" for="validationTooltip03">City</label>
                    <input type="text" class="form-control" id="validationTooltip03" required />
                    <div class="invalid-tooltip">
                      Please provide a valid city.
                    </div>
                  </b-col>
                  <b-col md="6" class="mb-3">
                    <label class="form-label" for="validationDefault04">State</label>
                    <select class="form-select" id="validationDefault04" required>
                      <option selected disabled value="">Choose...</option>
                      <option>...</option>
                    </select>
                  </b-col>
                  <b-col md="6" class="mb-3">
                    <label class="form-label" for="validationTooltip05">Zip</label>
                    <input type="text" class="form-control" id="validationTooltip05" required />
                    <div class="invalid-tooltip">
                      Please provide a valid zip.
                    </div>
                  </b-col>
                </b-row>
                <button class="btn btn-primary" type="submit">
                  Submit form
                </button>
              </form>
            </b-card-body>
          </iq-card>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
// import { socialvue } from '../../config/pluginInit'

export default {
  name: "FormValidates",
  mounted() {
    // socialvue.index()
  },
};
</script>
