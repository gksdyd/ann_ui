<template>
  <div class="content-inner">
    <b-container>
      <b-row>
        <b-col sm="12">
          <b-card
            no-body
            class="position-relative inner-page-bg bg-primary"
            style="height: 150px"
          >
            <div class="inner-page-title">
              <h3 class="text-white">Color Page</h3>
              <p class="text-white">lorem ipsum</p>
            </div>
          </b-card>
        </b-col>
        <b-col lg="12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">SocialV Color</h4>
            </template>

            <template v-slot:body>
              <p>
                Similar to the contextual text color classes, easily set the
                background of an element to any contextual class. Anchor
                components will darken on hover, just like the text classes.
                Background utilities
                <strong>do not set <code>color</code></strong
                >, so in some cases you’ll want to use
                <code>.text-*</code> utilities.
              </p>

              <b-row class="mt-4">
                <b-col lg="2" md="6" class="text-center mt-5 mt-lg-0">
                  <p class="bg-primary pt-5 pb-5 text-center rounded"></p>
                  <h6>Primary</h6>
                </b-col>
                <b-col lg="2" md="6" class="text-center mt-5 mt-lg-0">
                  <p class="bg-secondary pt-5 pb-5 text-center rounded"></p>
                  <h6>Secondary</h6>
                </b-col>
                <b-col lg="2" md="6" class="text-center mt-5 mt-lg-0">
                  <p class="bg-success pt-5 pb-5 text-center rounded"></p>
                  <h6>Success</h6>
                </b-col>
                <b-col lg="2" md="6" class="text-center mt-5 mt-lg-0">
                  <p class="bg-danger pt-5 pb-5 text-center rounded"></p>
                  <h6>Danger</h6>
                </b-col>
                <b-col lg="2" md="6" class="text-center mt-5 mt-lg-0">
                  <p class="bg-warning pt-5 pb-5 text-center rounded"></p>
                  <h6>Warning</h6>
                </b-col>
                <b-col lg="2" md="6" class="text-center mt-5 mt-lg-0">
                  <p class="bg-info pt-5 pb-5 text-center rounded"></p>
                  <h6>Info</h6>
                </b-col>
                <b-col lg="2" md="6" class="text-center mt-5 mt-lg-4">
                  <p class="bg-light pt-5 pb-5 text-center rounded"></p>
                  <h6>Light</h6>
                </b-col>
                <b-col lg="2" md="6" class="text-center mt-5 mt-lg-4">
                  <p class="bg-dark pt-5 pb-5 text-center rounded"></p>
                  <h6>Dark</h6>
                </b-col>
              </b-row>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">SocialV Color</h4>
            </template>
            <template v-slot:body>
              <p>
                Similar to the contextual text color classes, easily set the
                background of an element to any contextual class. Anchor
                components will darken on hover, just like the text classes.
                Background utilities
                <strong>do not set <code>color</code></strong
                >, so in some cases you’ll want to use
                <code>.text-*</code> utilities.
              </p>

              <b-row class="mt-4">
                <b-col lg="2" md="6" class="text-center">
                  <p
                    class="bg-primary-subtle text-primary pt-3 pb-3 text-center rounded font-size-18"
                  >
                    Primary
                  </p>
                </b-col>
                <b-col lg="2" md="6" class="text-center">
                  <p
                    class="bg-secondary-subtle text-secondary pt-3 pb-3 text-center rounded font-size-18"
                  >
                    Secondary
                  </p>
                </b-col>
                <b-col lg="2" md="6" class="text-center">
                  <p
                    class="bg-success-subtle text-success pt-3 pb-3 text-center rounded font-size-18"
                  >
                    Success
                  </p>
                </b-col>
                <b-col lg="2" md="6" class="text-center">
                  <p
                    class="bg-danger-subtle text-danger pt-3 pb-3 text-center rounded font-size-18"
                  >
                    Danger
                  </p>
                </b-col>
                <b-col lg="2" md="6" class="text-center">
                  <p
                    class="bg-warning-subtle text-warning pt-3 pb-3 text-center rounded font-size-18"
                  >
                    Warning
                  </p>
                </b-col>
                <b-col lg="2" md="6" class="text-center">
                  <p
                    class="bg-info-subtle text-info pt-4 pb-3 tex3-center rounded font-size-18"
                  >
                    Info
                  </p>
                </b-col>
                <b-col lg="2" md="6" class="text-center">
                  <p
                    class="bg-dark-subtle text-dark pt-4 pb-3 tex3-center rounded font-size-18 text-white"
                  >
                    Dark
                  </p>
                </b-col>
              </b-row>
            </template>
          </iq-card>
        </b-col>
        <b-col lg="6">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">SocialV Text Color</h4>
            </template>

            <template v-slot:body>
              <p>
                Contextual text classes also work well on anchors with the
                provided hover and focus states.
                <strong
                  >Note that the <code>.text-white</code> and
                  <code>.text-muted</code> class has no additional link styling
                  beyond underline.</strong
                >
              </p>

              <p class="text-primary">.text-primary</p>
              <p class="text-secondary">.text-secondary</p>
              <p class="text-success">.text-success</p>
              <p class="text-danger">.text-danger</p>
              <p class="text-warning">.text-warning</p>
              <p class="text-info">.text-info</p>
              <p class="text-light bg-dark">.text-light</p>
              <p class="text-dark">.text-dark</p>
              <p class="text-muted">.text-muted</p>
              <p class="text-white bg-dark">.text-white</p>
              <p class="text-black-50">.text-black-50</p>
              <p class="text-white-50 bg-dark mb-0">.text-white-50</p>
            </template>
          </iq-card>
        </b-col>
        <b-col lg="6">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">SocialV Text Color</h4>
            </template>

            <template v-slot:body>
              <p>
                Contextual text classes also work well on anchors with the
                provided hover and focus states.
                <strong
                  >Note that the <code>.text-white</code> and
                  <code>.text-muted</code> class has no additional link styling
                  beyond underline.</strong
                >
              </p>

              <p><a href="#" class="text-primary">Primary link</a></p>
              <p><a href="#" class="text-secondary">Secondary link</a></p>
              <p><a href="#" class="text-success">Success link</a></p>
              <p><a href="#" class="text-danger">Danger link</a></p>
              <p><a href="#" class="text-warning">Warning link</a></p>
              <p><a href="#" class="text-info">Info link</a></p>
              <p><a href="#" class="text-light bg-dark">Light link</a></p>
              <p><a href="#" class="text-dark">Dark link</a></p>
              <p><a href="#" class="text-muted">Muted link</a></p>
              <p class="mb-0">
                <a href="#" class="text-white bg-dark">White link</a>
              </p>
            </template>
          </iq-card>
        </b-col>
        <b-col lg="6">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">SocialV Text Color</h4>
            </template>

            <template v-slot:body>
              <p>
                Contextual text classes also work well on anchors with the
                provided hover and focus states.
                <strong
                  >Note that the <code>.text-white</code> and
                  <code>.text-muted</code> class has no additional link styling
                  beyond underline.</strong
                >
              </p>

              <p class="bg-primary-subtle ps-3 pe-3 pt-2 pb-2 rounded">
                Primary link
              </p>
              <p class="bg-secondary-subtle ps-3 pe-3 pt-2 pb-2 rounded">
                Secondary link
              </p>
              <p class="bg-success-subtle ps-3 pe-3 pt-2 pb-2 rounded">
                Success link
              </p>
              <p class="bg-danger-subtle ps-3 pe-3 pt-2 pb-2 rounded">
                Danger link
              </p>
              <p class="bg-warning-subtle ps-3 pe-3 pt-2 pb-2 rounded">
                Warning link
              </p>
              <p class="bg-info-subtle ps-3 pe-3 pt-2 pb-2 rounded">
                Info link
              </p>
              <p class="bg-dark-subtle ps-3 pe-3 pt-2 pb-2 rounded mb-0">
                Dark link
              </p>
            </template>
          </iq-card>
        </b-col>
        <b-col lg="6">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">SocialV Text Color</h4>
            </template>

            <template v-slot:body>
              <p>
                Contextual text classes also work well on anchors with the
                provided hover and focus states.
                <strong
                  >Note that the <code>.text-white</code> and
                  <code>.text-muted</code> class has no additional link styling
                  beyond underline.</strong
                >
              </p>

              <p>
                <a
                  href="#"
                  class="bg-primary-subtle ps-3 pe-3 pt-2 pb-2 rounded d-inline-block"
                  >Primary link</a
                >
              </p>
              <p>
                <a
                  href="#"
                  class="bg-secondary-subtle ps-3 pe-3 pt-2 pb-2 rounded d-inline-block"
                  >Secondary link</a
                >
              </p>
              <p>
                <a
                  href="#"
                  class="bg-success-subtle ps-3 pe-3 pt-2 pb-2 rounded d-inline-block"
                  >Success link</a
                >
              </p>
              <p>
                <a
                  href="#"
                  class="bg-danger-subtle ps-3 pe-3 pt-2 pb-2 rounded d-inline-block"
                  >Danger link</a
                >
              </p>
              <p>
                <a
                  href="#"
                  class="bg-warning-subtle ps-3 pe-3 pt-2 pb-2 rounded d-inline-block"
                  >Warning link</a
                >
              </p>
              <p>
                <a
                  href="#"
                  class="bg-info-subtle ps-3 pe-3 pt-2 pb-2 rounded d-inline-block"
                  >Info link</a
                >
              </p>
              <p class="mb-0">
                <a
                  href="#"
                  class="bg-dark-subtle ps-3 pe-3 pt-2 pb-2 rounded d-inline-block"
                  >Dark link</a
                >
              </p>
            </template>
          </iq-card>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>
<script>
// import { socialvue } from '../../config/pluginInit'

export default {
  name: "UiColor",
  mounted() {
    // socialvue.index()
  },
};
</script>
