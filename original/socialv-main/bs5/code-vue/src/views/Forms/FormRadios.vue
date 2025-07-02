<template>
  <div class="content-inner">
    <b-container>
      <div class="row">
        <div class="col-sm-12">
          <div class="position-relative inner-page-bg bg-primary card" style="height: 150px;">
            <div class="inner-page-title">
              <h3 class="text-white">Form Radio Page</h3>
              <p class="text-white">lorem ipsum</p>
            </div>
          </div>
        </div>
        <div class="col-lg-6 col-sm-12">
          <div class="card">
            <div class="d-flex justify-content-between card-header">
              <div class="header-title">
                <h4 class="card-title">Default Radio Buttons</h4>
              </div>
            </div>
            <div class="pt-0 card-body">
              <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi vulputate, ex ac venenatis mollis, diam
                nibh finibus leo</p>
              <div class="form-check radio form-check-inline"><input type="radio" name="bsradio" id="radio1"
                  checked=""><label for="radio1">Active</label></div>{{ "" }}
              <div class="form-check radio form-check-inline"><input type="radio" name="bsradio" id="radio2"><label
                  for="radio2">Inactive</label></div>{{ "" }}
              <div class="form-check radio form-check-inline"><input type="radio" name="bsradio1" id="radio3"
                  disabled="" checked=""><label for="radio3">Active - Disabled</label></div>{{ "" }}
              <div class="form-check radio form-check-inline"><input type="radio" name="bsradio1" id="radio4"
                  disabled=""><label for="radio3">Inactive - Disabled</label></div>{{ "" }}
            </div>
          </div>
          <div class="card">
            <div class="d-flex justify-content-between card-header">
              <div class="header-title">
                <h4 class="card-title">Custom Colored Radio Buttons</h4>
              </div>
            </div>
            <div class="pt-0 card-body">
              <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi vulputate, ex ac venenatis mollis, diam
                nibh finibus leo</p>
              <div class="form-check custom-radio custom-radio-color form-check-inline form-check"><input
                  name="customRadio-11" type="radio" id="customRadio01"
                  class="form-check-input bg-primary form-check-input"><label class="form-check-label form-check-label">
                  Primary </label></div>{{ "" }}
              <div class="form-check custom-radio custom-radio-color form-check-inline form-check"><input
                  name="customRadio-11" type="radio" id="customRadio02"
                  class="form-check-input bg-success form-check-input"><label class="form-check-label form-check-label">
                  Success </label></div>{{ "" }}
              <div class="form-check custom-radio custom-radio-color form-check-inline form-check"><input
                  name="customRadio-11" type="radio" id="customRadio03"
                  class="form-check-input bg-danger form-check-input"><label class="form-check-label form-check-label">
                  Danger </label></div>{{ "" }}
              <div class="form-check custom-radio custom-radio-color form-check-inline form-check"><input
                  name="customRadio-11" type="radio" id="customRadio04"
                  class="form-check-input bg-warning form-check-input"><label class="form-check-label form-check-label">
                  Warning </label></div>{{ "" }}
              <div class="form-check custom-radio custom-radio-color form-check-inline form-check"><input
                  name="customRadio-11" type="radio" id="customRadio05"
                  class="form-check-input bg-dark form-check-input"><label class="form-check-label form-check-label">
                  Dark </label></div>{{ "" }}
              <div class="form-check custom-radio custom-radio-color form-check-inline form-check"><input
                  name="customRadio-11" type="radio" id="customRadio06"
                  class="form-check-input bg-info form-check-input"><label class="form-check-label form-check-label">
                  Info </label></div>{{ "" }}
            </div>
          </div>
        </div>
        <div class="col-lg-6 col-sm-12">
          <div class="card">
            <div class="d-flex justify-content-between card-header">
              <div class="header-title">
                <h4 class="card-title">Custom Radio Buttons</h4>
              </div>
            </div>
            <div class="pt-0 card-body">
              <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi vulputate, ex ac venenatis mollis, diam
                nibh finibus leo</p>
              <div class="form-check custom-radio form-check-inline form-check"><input name="customRadio-1" type="radio"
                  id="customRadio6" class="form-check-input form-check-input"><label
                  class="form-check-label form-check-label"> One </label></div>{{ "" }}
              <div class="form-check custom-radio form-check-inline form-check"><input name="customRadio-1" type="radio"
                  id="customRadio7" class="form-check-input form-check-input"><label
                  class="form-check-label form-check-label"> Two </label></div>{{ "" }}
              <div class="form-check custom-radio form-check-inline form-check"><input name="customRadio-1" type="radio"
                  id="customRadio8" class="form-check-input form-check-input" checked=""><label
                  class="form-check-label form-check-label"> Three </label></div>{{ "" }}
              <div class="form-check custom-radio form-check-inline form-check"><input name="customRadio-2" type="radio"
                  id="customRadio-8" class="form-check-input form-check-input" checked=""><label
                  class="form-check-label form-check-label"> Four Checked </label></div>{{ "" }}
              <div class="form-check custom-radio form-check-inline form-check"><input name="customRadio-3" disabled=""
                  type="radio" id="customRadio9" class="form-check-input form-check-input"><label
                  class="form-check-label form-check-label"> Five disabled</label></div>{{ "" }}
              <div class="form-check custom-radio form-check-inline form-check"><input name="customRadio-4" disabled=""
                  type="radio" id="customRadio10" class="form-check-input form-check-input" checked=""><label
                  class="form-check-label form-check-label"> Six Selected and disabled</label></div>{{ "" }}
            </div>
          </div>
          <div class="card">
            <div class="d-flex justify-content-between card-header">
              <div class="header-title">
                <h4 class="card-title">Colored Radio Buttons</h4>
              </div>
            </div>
            <div class="pt-0 card-body">
              <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi vulputate, ex ac venenatis mollis, diam
                nibh finibus leo</p>
              <div class="form-check custom-radio custom-radio-color-defaultChecked form-check-inline form-check"><input
                  name="customRadio-10" type="radio" id="customRadio-1" class="form-check-input form-check-input"><label
                  class="form-check-label form-check-label"> Primary </label></div>{{ "" }}
              <div class="form-check custom-radio custom-radio-color-defaultChecked form-check-inline form-check"><input
                  name="customRadio-10" type="radio" id="customRadio-2" class="form-check-input form-check-input"><label
                  class="form-check-label form-check-label"> Success </label></div>{{ "" }}
              <div class="form-check custom-radio custom-radio-color-defaultChecked form-check-inline form-check"><input
                  name="customRadio-10" type="radio" id="customRadio-3" class="form-check-input form-check-input"><label
                  class="form-check-label form-check-label"> Danger </label></div>{{ "" }}
              <div class="form-check custom-radio custom-radio-color-defaultChecked form-check-inline form-check"><input
                  name="customRadio-10" type="radio" id="customRadio-4" class="form-check-input form-check-input"><label
                  class="form-check-label form-check-label"> Warning </label></div>{{ "" }}
              <div class="form-check custom-radio custom-radio-color-defaultChecked form-check-inline form-check"><input
                  name="customRadio-10" type="radio" id="customRadio-5" class="form-check-input form-check-input"><label
                  class="form-check-label form-check-label"> Dark </label></div>{{ "" }}
              <div class="form-check custom-radio custom-radio-color-defaultChecked form-check-inline form-check"><input
                  name="customRadio-10" type="radio" id="customRadio-6" class="form-check-input form-check-input"><label
                  class="form-check-label form-check-label"> Info </label></div>{{ "" }}
            </div>
          </div>
        </div>
      </div>
    </b-container>
  </div>
</template>
<script>
// import { socialvue } from '../../config/pluginInit'

export default {
  name: "FormRadios",
  mounted() {
    // socialvue.index()
  },
};
</script>
