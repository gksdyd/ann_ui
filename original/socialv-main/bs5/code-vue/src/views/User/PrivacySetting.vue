<template>
  <div class="content-inner" id="page_layout">
    <b-container>
      <b-row>
        <b-col lg="12">
          <iq-card>
            <template v-slot:headerTitle>
              <h4 class="card-title">Privacy Setting</h4>
            </template>
            <template v-slot:body>
              <div class="acc-privacy">
                <div class="data-privacy">
                  <h4 class="mb-2">Account Privacy</h4>
                  <div class="form-check form-check-inline">
                    <input
                      type="checkbox"
                      class="form-check-input"
                      id="acc-private"
                    />
                    <label
                      class="form-check-label privacy-status mb-2"
                      for="acc-private"
                      >Private Account</label
                    >
                  </div>
                  <p>
                    Lorem Ipsum is simply dummy text of the printing and
                    typesetting industry. Lorem Ipsum has been the industry's
                    standard dummy text ever since the 1500s, when an unknown
                    printer took a galley of type and scrambled it to make a
                    type specimen book
                  </p>
                </div>
                <hr />
                <div class="data-privacy">
                  <h4 class="mb-2">Activity Status</h4>
                  <div class="form-check form-check-inline">
                    <input
                      type="checkbox"
                      class="form-check-input"
                      id="activety"
                      checked=""
                    />
                    <label
                      class="form-check-label privacy-status mb-2"
                      for="activety"
                      >Show Activity Status</label
                    >
                  </div>
                  <p>
                    It is a long established fact that a reader will be
                    distracted by the readable content of a page when looking at
                    its layout. The point of using Lorem Ipsum is that it has a
                    more-or-less normal distribution of letters, as opposed to
                    using 'Content here, content here', making it look like
                    readable English.
                  </p>
                </div>
                <hr />
                <div class="data-privacy">
                  <h4 class="mb-2">Story Sharing</h4>
                  <div class="form-check form-check-inline">
                    <input
                      type="checkbox"
                      class="form-check-input"
                      id="story"
                      checked=""
                    />
                    <label
                      class="form-check-label privacy-status mb-2"
                      for="story"
                      >Allow Sharing</label
                    >
                  </div>
                  <p>
                    It is a long established fact that a reader will be
                    distracted by the readable content of a page when looking at
                    its layout. The point of using Lorem Ipsum is that it has a
                    more-or-less normal distribution of letters, as opposed to
                    using 'Content here, content here', making it look like
                    readable English.
                  </p>
                </div>
                <hr />
                <div class="data-privacy">
                  <h4 class="mb-2">Photo Of You</h4>
                  <div class="custom-control custom-radio">
                    <input
                      type="radio"
                      id="automatically"
                      name="customRadio0"
                      class="form-check-input"
                      checked=""
                    />
                    {{ "" }}
                    <label class="form-check-label" for="automatically">
                      Add Automatically</label
                    >
                  </div>
                  <div class="custom-control custom-radio mb-2">
                    <input
                      type="radio"
                      id="manualy"
                      name="customRadio0"
                      class="form-check-input"
                    />
                    {{ "" }}
                    <label class="form-check-label" for="manualy">
                      Add Manualy</label
                    >
                  </div>
                  <p>
                    It is a long established fact that a reader will be
                    distracted by the readable content of a page when looking at
                    its layout. The point of using Lorem Ipsum is that it has a
                    more-or-less normal distribution of letters, as opposed to
                    using 'Content here, content here', making it look like
                    readable English.
                  </p>
                </div>
                <hr />
                <div class="data-privacy">
                  <h4 class="mb-2">Your Profile</h4>
                  <div class="custom-control custom-radio">
                    <input
                      type="radio"
                      id="public"
                      name="customRadio1"
                      class="form-check-input"
                      checked=""
                    />
                    {{ "" }}
                    <label class="form-check-label" for="public">
                      Public
                    </label>
                  </div>
                  <div class="custom-control custom-radio">
                    <input
                      type="radio"
                      id="friend"
                      name="customRadio1"
                      class="form-check-input"
                    />
                    {{ "" }}
                    <label class="form-check-label" for="friend">
                      Friend
                    </label>
                  </div>
                  <div class="custom-control custom-radio">
                    <input
                      type="radio"
                      id="spfriend"
                      name="customRadio1"
                      class="form-check-input"
                    />
                    {{ "" }}
                    <label class="form-check-label" for="spfriend">
                      Specific Friend
                    </label>
                  </div>
                  <div class="custom-control custom-radio mb-2">
                    <input
                      type="radio"
                      id="onlyme"
                      name="customRadio1"
                      class="form-check-input"
                    />
                    {{ "" }}
                    <label class="form-check-label" for="onlyme">
                      Only Me
                    </label>
                  </div>
                  <p>
                    It is a long established fact that a reader will be
                    distracted by the readable content of a page when looking at
                    its layout. The point of using Lorem Ipsum is that it has a
                    more-or-less normal distribution of letters, as opposed to
                    using 'Content here, content here', making it look like
                    readable English.
                  </p>
                </div>
                <hr />
                <div class="data-privacy">
                  <h4 class="mb-2">Login Notification</h4>
                  <div class="custom-control custom-radio">
                    <input
                      type="radio"
                      id="enable"
                      name="customRadio2"
                      class="form-check-input"
                    />
                    {{ "" }}
                    <label class="form-check-label" for="enable">
                      Enable
                    </label>
                  </div>
                  <div class="custom-control custom-radio mb-2">
                    <input
                      type="radio"
                      id="disable"
                      name="customRadio2"
                      class="form-check-input"
                      checked=""
                    />
                    {{ "" }}
                    <label class="form-check-label" for="disable">
                      Disable
                    </label>
                  </div>
                  <p>
                    It is a long established fact that a reader will be
                    distracted by the readable content of a page when looking at
                    its layout. The point of using Lorem Ipsum is that it has a
                    more-or-less normal distribution of letters, as opposed to
                    using 'Content here, content here', making it look like
                    readable English.
                  </p>
                </div>
                <hr />
                <div class="data-privacy">
                  <h4 class="mb-2">Privacy Help</h4>
                  <a href="#" class="d-flex align-items-center"
                    ><span class="material-symbols-outlined">support_agent</span
                    ><span class="ms-2">Support</span></a
                  >
                </div>
              </div>
            </template>
          </iq-card>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>
<script>
export default {
  name: "PrivacySetting",
};
</script>
