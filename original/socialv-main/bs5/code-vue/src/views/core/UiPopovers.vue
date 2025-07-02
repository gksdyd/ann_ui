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
              <h3 class="text-white">Popovers Page</h3>
              <p class="text-white">lorem ipsum</p>
            </div>
          </b-card>
        </b-col>
        <b-col lg="6" sm="12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Popovers</h4>
            </template>
            <template v-slot:headerAction> </template>
            <template v-slot:body>
              <p>
                Lorem Ipsum is simply dummy text of the printing and typesetting
                industry.
              </p>
              <popover
                tabindex="0"
                role="button"
                className="btn-lg btn-danger"
                data-bs-toggle="popover"
                data-trigger="focus"
                popoverContent="And heres some amazing content. It's very engaging. Right?"
                title="Popover title"
                >Click to toggle popover</popover
              >
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Dismiss on next click</h4>
            </template>
            <template v-slot:headerAction> </template>
            <template v-slot:body>
              <p>
                Use the <code>focus</code> trigger to dismiss popovers on the
                user’s next click of a different element than the toggle
                element.
              </p>
              <popover
                className="btn-danger"
                title="Dismissible popover"
                popoverTrigger="focus"
                popoverContent="And here's some amazing content. It's very engaging. Right?"
                >Dismissible popover</popover
              >
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Disabled elements</h4>
            </template>
            <template v-slot:headerAction> </template>
            <template v-slot:body>
              <p>
                Elements with the <code>disabled</code> attribute aren’t
                interactive, meaning users cannot hover or click them to trigger
                a popover (or tooltip). As a workaround, you’ll want to trigger
                the popover from a wrapper <code>&lt;div&gt;</code> or
                <code>&lt;span&gt;</code> and override the
                <code>pointer-events</code> on the disabled element.
              </p>
              <!-- Coming Soon -->
              <span
                class="d-inline-block"
                tabindex="0"
                title="Disabled popover"
              >
                <popover className="btn-primary" title="Popover title" disabled
                  >Disabled button</popover
                >
              </span>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Hover elements</h4>
            </template>
            <template v-slot:headerAction> </template>
            <template v-slot:body>
              <p>
                For disabled popover triggers, you may also prefer
                <code>data-trigger="hover"</code> so that the popover appears as
                immediate visual feedback to your users as they may not expect
                to <em>click</em> on a disabled element.
              </p>
              <span
                class="d-inline-block"
                tabindex="0"
                title="Disabled popover"
              >
                <popover className="btn-primary" title="Popover title" disabled
                  >Disabled button</popover
                >
              </span>
            </template>
          </iq-card>
        </b-col>
        <b-col lg="6" sm="12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Four directions</h4>
            </template>
            <template v-slot:headerAction> </template>
            <template v-slot:body>
              <p>
                Four options are available: top, right, bottom, and left
                aligned.
              </p>
              <popover
                className="btn-secondary mb-1"
                popoverContent="Vivamus sagittis lacus vel augue laoreet rutrum faucibus."
                popoverPlacement="top"
                >Popover on top</popover
              >
              {{ "" }}
              <popover
                className="btn-secondary mb-1"
                popoverContent="Vivamus sagittis lacus vel augue laoreet rutrum faucibus."
                popoverPlacement="right"
                >Popover on right</popover
              >
              {{ "" }}
              <popover
                className="btn-secondary mb-1"
                popoverContent="Vivamus sagittis lacus vel augue laoreet rutrum faucibus."
                popoverPlacement="bottom"
                >Popover on bottom</popover
              >
              {{ "" }}
              <popover
                className="btn-secondary mb-1"
                popoverContent="Vivamus sagittis lacus vel augue laoreet rutrum faucibus."
                popoverPlacement="left"
                >Popover on left</popover
              >
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Popovers With Color</h4>
            </template>
            <template v-slot:headerAction> </template>
            <template v-slot:body>
              <p>
                Four options are available: top, right, bottom, and left
                aligned.
              </p>
              <!-- Coming Soon -->
              <popover
                className="btn-primary mb-1"
                popoverContent="Vivamus sagittis lacus vel augue laoreet rutrum faucibus."
                popoverPlacement="top"
                >Popover on top</popover
              >
              {{ "" }}
              <popover
                className="btn-success mb-1"
                popoverContent="Vivamus sagittis lacus vel augue laoreet rutrum faucibus."
                popoverPlacement="right"
                >Popover on right</popover
              >
              {{ "" }}
              <popover
                className="btn-danger mb-1"
                popoverContent="Vivamus sagittis lacus vel augue laoreet rutrum faucibus."
                popoverPlacement="bottom"
                >Popover on bottom</popover
              >
              {{ "" }}
              <popover
                className="btn-info mb-1"
                popoverContent="Vivamus sagittis lacus vel augue laoreet rutrum faucibus."
                popoverPlacement="left"
                >Popover on left</popover
              >
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Popovers With Color</h4>
            </template>
            <template v-slot:headerAction> </template>
            <template v-slot:body>
              <p>
                Four options are available: top, right, bottom, and left
                aligned.
              </p>
              <!-- Coming Soon -->
              <popover
                className="btn btn-primary-subtle mb-1 me-1"
                popoverContent="Vivamus sagittis lacus vel augue laoreet rutrum faucibus."
                popoverPlacement="top"
                >Popover on top</popover
              >
              <popover
                className="btn btn-success-subtle mb-1 me-1"
                popoverContent="Vivamus sagittis lacus vel augue laoreet rutrum faucibus."
                popoverPlacement="right"
                >Popover on right</popover
              >
              <popover
                className="btn btn-danger-subtle mb-1 me-1"
                popoverContent="Vivamus sagittis lacus vel augue laoreet rutrum faucibus."
                popoverPlacement="bottom"
                >Popover on bottom</popover
              >
              <popover
                className="btn btn-info-subtle mb-1 me-1"
                popoverContent="Vivamus sagittis lacus vel augue laoreet rutrum faucibus."
                popoverPlacement="left"
                >Popover on left</popover
              >
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
  name: "UiPopovers",
  mounted() {
    // socialvue.index()
  },
};
</script>
