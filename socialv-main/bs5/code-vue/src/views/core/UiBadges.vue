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
              <h3 class="text-white">Badges Page</h3>
              <p class="text-white">lorem ipsum</p>
            </div>
          </b-card>
        </b-col>
        <b-col lg="6" sm="12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Badge</h4>
            </template>
            <template v-slot:body>
              <p>
                Badges scale to match the size of the immediate parent element
                by using relative font sizing and <code>em</code> units.
              </p>
              <h1 class="mb-3">
                Example heading <span class="badge bg-primary">New</span>
              </h1>
              <h2 class="mb-3">
                Example heading <span class="badge bg-secondary">New</span>
              </h2>
              <h3 class="mb-3">
                Example heading
                <button class="btn btn-success">
                  Notifications
                  <span class="badge bg-light text-dark ml-2">4</span>
                </button>
              </h3>
              <h4 class="mb-3">
                Example heading <span class="badge bg-danger">New</span>
              </h4>
              <h5 class="mb-3">
                Example heading <span class="badge bg-warning">New</span>
              </h5>
              <h6 class="mb-0">
                Example heading <span class="badge bg-info">New</span>
              </h6>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Button Badges</h4>
            </template>
            <template v-slot:body>
              <p>Badges can be used as part of buttons to provide a counter.</p>
              <button type="button" class="btn mb-1 btn-primary">
                Notifications
                <span class="badge bg-light text-dark ml-2">4</span>
              </button>
              {{ "" }}
              <button type="button" class="btn mb-1 btn-success">
                Notifications
                <span class="badge bg-light text-dark ml-2">4</span>
              </button>
              {{ "" }}
              <button type="button" class="btn mb-1 btn-danger">
                Notifications
                <span class="badge bg-light text-dark ml-2">4</span>
              </button>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Button Light background Badges</h4>
            </template>
            <template v-slot:body>
              <p>Badges can be used as part of buttons to provide a counter.</p>
              <button type="button" class="btn mb-1 btn-outline-primary">
                Notifications
                <span class="badge bg-primary ml-2">4</span>
              </button>
              {{ "" }}
              <button type="button" class="btn mb-1 btn-outline-success">
                Notifications
                <span class="badge bg-success ml-2">4</span>
              </button>
              {{ "" }}
              <button type="button" class="btn mb-1 btn-outline-danger">
                Notifications
                <span class="badge bg-danger ml-2">4</span>
              </button>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Button Border Badges</h4>
            </template>
            <template v-slot:body>
              <p>Badges can be used as part of buttons to provide a counter.</p>
              <button type="button" class="btn mb-1 btn-primary-subtle">
                Notifications <span class="badge bg-primary ml-2">4</span>
              </button>
              {{ "" }}
              <button type="button" class="btn mb-1 btn-success-subtle">
                Notifications <span class="badge bg-success ml-2">4</span>
              </button>
              {{ "" }}
              <button type="button" class="btn mb-1 btn-danger-subtle">
                Notifications <span class="badge bg-danger ml-2">4</span>
              </button>
            </template>
          </iq-card>
        </b-col>
        <b-col lg="6" sm="12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Contextual variations</h4>
            </template>
            <template v-slot:body>
              <p class="mb-0">
                Add any of the below mentioned modifier classes to change the
                appearance of a badge.
              </p>
              <span class="badge bg-primary mt-2">Primary</span>
              {{ "" }}
              <span class="badge bg-secondary mt-2">Secondary</span>
              {{ "" }}
              <span class="badge bg-success mt-2">Success</span>
              {{ "" }}
              <span class="badge bg-danger mt-2">Danger</span>
              {{ "" }}
              <span class="badge bg-warning mt-2">Warning</span>
              {{ "" }}
              <span class="badge bg-info mt-2">Info</span>
              {{ "" }}
              <span class="badge bg-light mt-2">Light</span>
              {{ "" }}
              <span class="badge bg-dark mt-2">Dark</span>
              {{ "" }}
              <h5 class="card-title mt-4">Pill badges</h5>
              <p class="mb-0">
                Use the <code>.badge-pill</code> modifier class to make badges
                more rounded (with a larger <code>border-radius</code> and
                additional horizontal <code>padding</code>). Useful if you miss
                the badges from v3.
              </p>
              <span class="badge bg-primary mt-2">Primary</span>
              {{ "" }}
              <span class="badge bg-secondary mt-2">Secondary</span>
              {{ "" }}
              <span class="badge bg-success mt-2">Success</span>
              {{ "" }}
              <span class="badge bg-danger mt-2">Danger</span>
              {{ "" }}
              <span class="badge bg-warning mt-2">Warning</span>
              {{ "" }}
              <span class="badge bg-info mt-2">Info</span>
              {{ "" }}
              <span class="badge bg-light mt-2">Light</span>
              {{ "" }}
              <span class="badge bg-dark mt-2">Dark</span>
              {{ "" }}
              <h5 class="card-title mt-4">Links</h5>
              <p class="mb-0">
                Using the contextual <code>.badge-*</code> classes on an
                <code>&lt;a&gt;</code> element quickly provide
                <em>actionable</em> badges with hover and focus states.
              </p>
              <span class="badge bg-primary mt-2">Primary</span>
              {{ "" }}
              <span class="badge bg-secondary mt-2">Secondary</span>
              {{ "" }}
              <span class="badge bg-success mt-2">Success</span>
              {{ "" }}
              <span class="badge bg-danger mt-2">Danger</span>
              {{ "" }}
              <span class="badge bg-warning mt-2">Warning</span>
              {{ "" }}
              <span class="badge bg-info mt-2">Info</span>
              {{ "" }}
              <span class="badge bg-light mt-2">Light</span>
              {{ "" }}
              <span class="badge bg-dark mt-2">Dark</span>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Contextual variations Border</h4>
            </template>
            <template v-slot:body>
              <p class="mb-0">
                Add any of the below mentioned modifier classes to change the
                appearance of a badge.
              </p>
              <span class="badge border border-primary text-primary mt-2"
                >Primary</span
              >
              {{ "" }}
              <span class="badge border border-secondary text-secondary mt-2"
                >Secondary</span
              >
              {{ "" }}
              <span class="badge border border-success text-success mt-2"
                >Success</span
              >
              {{ "" }}
              <span class="badge border border-danger text-danger mt-2"
                >Danger</span
              >
              {{ "" }}
              <span class="badge border border-warning text-warning mt-2"
                >Warning</span
              >
              {{ "" }}
              <span class="badge border border-info text-info mt-2">Info</span>
              {{ "" }}
              <span class="badge border border-light text-light mt-2"
                >Light</span
              >
              {{ "" }}
              <span class="badge border border-dark text-dark mt-2">Dark</span>
              <h5 class="card-title mt-4">Pill badges</h5>
              <p class="mb-0">
                Use the <code>.badge-pill</code> modifier class to make badges
                more rounded (with a larger <code>border-radius</code> and
                additional horizontal <code>padding</code>). Useful if you miss
                the badges from v3.
              </p>
              <span
                class="badge border rounded-pill border-primary text-primary mt-2"
                >Primary</span
              >{{ "" }}
              <span
                class="badge border rounded-pill border-secondary text-secondary mt-2"
                >Secondary</span
              >{{ "" }}
              <span
                class="badge border rounded-pill border-success text-success mt-2"
                >Success</span
              >{{ "" }}
              <span
                class="badge border rounded-pill border-danger text-danger mt-2"
                >Danger</span
              >{{ "" }}
              <span
                class="badge border rounded-pill border-warning text-warning mt-2"
                >Warning</span
              >{{ "" }}
              <span class="badge border rounded-pill border-info text-info mt-2"
                >Info</span
              >{{ "" }}
              <span
                class="badge border rounded-pill border-light text-light mt-2"
                >Light</span
              >{{ "" }}
              <span class="badge border rounded-pill border-dark text-dark mt-2"
                >Dark</span
              >
              <h5 class="card-title mt-4">Links</h5>
              <p class="mb-0">
                Using the contextual <code>.badge-*</code> classes on an
                <code>&lt;a&gt;</code> element quickly provide
                <em>actionable</em> badges with hover and focus states.
              </p>
              <span class="badge border border-primary text-primary mt-2"
                >Primary</span
              >{{ "" }}
              <span class="badge border border-secondary text-secondary mt-2"
                >Secondary</span
              >{{ "" }}
              <span class="badge border border-success text-success mt-2"
                >Success</span
              >{{ "" }}
              <span class="badge border border-danger text-danger mt-2"
                >Danger</span
              >{{ "" }}
              <span class="badge border border-warning text-warning mt-2"
                >Warning</span
              >{{ "" }}
              <span class="badge border border-info text-info mt-2">Info</span
              >{{ "" }}
              <span class="badge border border-light text-light mt-2"
                >Light</span
              >{{ "" }}
              <span class="badge border border-dark text-dark mt-2">Dark</span>
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
  name: "UiBadges",
  mounted() {
    // socialvue.index()
  },
};
</script>
