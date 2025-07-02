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
              <h3 class="text-white">Notification Page</h3>
              <p class="text-white">lorem ipsum</p>
            </div>
          </b-card>
        </b-col>
        <b-col lg="6">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Notifications</h4>
            </template>

            <template v-slot:body>
              <p>
                Toasts are as flexible as you need and have very little required
                markup. At a minimum, we require a single element to contain
                your “toasted” content and strongly encourage a dismiss button.
              </p>

              <toast class="fade show">
                <toast-header>
                  <svg
                    class="bd-placeholder-img rounded me-2"
                    width="20"
                    height="20"
                    xmlns="http://www.w3.org/2000/svg"
                    preserveAspectRatio="xMidYMid slice"
                    focusable="false"
                    role="img"
                  >
                    <rect width="100%" height="100%" fill="#007aff"></rect>
                  </svg>
                  <strong class="me-auto">Bootstrap</strong>
                  <small>11 mins ago</small>
                  <button
                    :dismissable="true"
                    type="button"
                    :class="`ms-2 mb-1 btn-close  ${buttonClass}`"
                    data-bs-dismiss="toast"
                    aria-label="Close"
                  ></button>
                </toast-header>
                <toast-body>
                  Hello, world! This is a toast message.
                </toast-body>
              </toast>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Stacking</h4>
            </template>

            <template v-slot:body>
              <p>
                When you have multiple toasts, we default to vertically stacking
                them in a readable manner.
              </p>

              <toast class="fade show mb-2">
                <toast-header>
                  <svg
                    class="bd-placeholder-img rounded me-2"
                    width="20"
                    height="20"
                    xmlns="http://www.w3.org/2000/svg"
                    preserveAspectRatio="xMidYMid slice"
                    focusable="false"
                    role="img"
                  >
                    <rect width="100%" height="100%" fill="#007aff"></rect>
                  </svg>
                  <strong class="me-auto">Bootstrap</strong>
                  <small class="text-muted">just now</small>
                  <button
                    :dismissable="true"
                    type="button"
                    :class="`ms-2 mb-1 btn-close ${buttonClass}`"
                    data-bs-dismiss="toast"
                    aria-label="Close"
                  ></button>
                </toast-header>
                <toast-body> See? Just like this. </toast-body>
              </toast>
              <toast class="fade show">
                <toast-header>
                  <svg
                    class="bd-placeholder-img rounded me-2"
                    width="20"
                    height="20"
                    xmlns="http://www.w3.org/2000/svg"
                    preserveAspectRatio="xMidYMid slice"
                    focusable="false"
                    role="img"
                  >
                    <rect width="100%" height="100%" fill="#007aff"></rect>
                  </svg>
                  <strong class="me-auto">Bootstrap</strong>
                  <small class="text-muted">2 seconds ago</small>
                  <button
                    :dismissable="true"
                    type="button"
                    :class="`btn-close ms-2 mb-1 ${buttonClass}`"
                    data-bs-dismiss="toast"
                    aria-label="Close"
                  ></button>
                </toast-header>
                <toast-body>
                  Heads up, toasts will stack automatically
                </toast-body>
              </toast>
            </template>
          </iq-card>

          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">
                Notifications horizontally and/or vertically
              </h4>
            </template>

            <template v-slot:body>
              <p>
                You can also get fancy with flexbox utilities to align toasts
                horizontally and/or vertically.
              </p>

              <div class="p-3 bg-dark">
                <div
                  aria-live="polite"
                  aria-atomic="true"
                  class="d-flex justify-content-center align-items-center"
                  style="min-height: 200px"
                >
                  <toast class="fade show">
                    <toast-header>
                      <svg
                        class="bd-placeholder-img rounded me-2"
                        width="20"
                        height="20"
                        xmlns="http://www.w3.org/2000/svg"
                        preserveAspectRatio="xMidYMid slice"
                        focusable="false"
                        role="img"
                      >
                        <rect width="100%" height="100%" fill="#007aff"></rect>
                      </svg>
                      <strong class="me-auto">Bootstrap</strong>
                      <small>11 mins ago</small>
                      <button
                        :dismissable="true"
                        type="button"
                        :class="`btn-close  ms-2 mb-1 ${buttonClass}`"
                        data-bs-dismiss="toast"
                        aria-label="Close"
                      ></button>
                    </toast-header>
                    <toast-body>
                      Hello, world! This is a toast message.
                    </toast-body>
                  </toast>
                </div>
              </div>
            </template>
          </iq-card>
        </b-col>
        <b-col lg="6">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Notifications</h4>
            </template>

            <template v-slot:body>
              <p>
                Toasts are slightly translucent, too, so they blend over
                whatever they might appear over. For browsers that support the
                <code>backdrop-filter</code> CSS property, we’ll also attempt to
                blur the elements under a toast.
              </p>

              <div class="p-3 bg-dark">
                <toast class="fade show">
                  <toast-header>
                    <svg
                      class="bd-placeholder-img rounded me-2"
                      width="20"
                      height="20"
                      xmlns="http://www.w3.org/2000/svg"
                      preserveAspectRatio="xMidYMid slice"
                      focusable="false"
                      role="img"
                    >
                      <rect width="100%" height="100%" fill="#007aff"></rect>
                    </svg>
                    <strong class="me-auto">Bootstrap</strong>
                    <small>11 mins ago</small>
                    <button
                      :dismissable="true"
                      type="button"
                      :class="`btn-close  ms-2 mb-1 ${buttonClass}`"
                      data-bs-dismiss="toast"
                      aria-label="Close"
                    ></button>
                  </toast-header>
                  <toast-body>
                    Hello, world! This is a toast message.
                  </toast-body>
                </toast>
              </div>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Stacking Placement</h4>
            </template>

            <template v-slot:body>
              <p>
                Place toasts with custom CSS as you need them. The top right is
                often used for notifications, as is the top middle. If you’re
                only ever going to show one toast at a time, put the positioning
                styles right on the <code>.toast</code>.
              </p>
              <div class="p-3 bg-dark">
                <div
                  aria-live="polite"
                  aria-atomic="true"
                  style="position: relative; min-height: 200px"
                >
                  <toast
                    class="fade show"
                    style="position: absolute; top: 0; right: 0"
                  >
                    <toast-header>
                      <svg
                        class="bd-placeholder-img rounded me-2"
                        width="20"
                        height="20"
                        xmlns="http://www.w3.org/2000/svg"
                        preserveAspectRatio="xMidYMid slice"
                        focusable="false"
                        role="img"
                      >
                        <rect width="100%" height="100%" fill="#007aff"></rect>
                      </svg>
                      <strong class="me-auto">Bootstrap</strong>
                      <small>11 mins ago</small>
                      <button
                        :dismissable="true"
                        type="button"
                        :class="`btn-close ms-2 mb-1 ${buttonClass}`"
                        data-bs-dismiss="toast"
                        aria-label="Close"
                      ></button>
                    </toast-header>
                    <toast-body>
                      Hello, world! This is a toast message.
                    </toast-body>
                  </toast>
                </div>
              </div>
              <p class="mt-3">
                For systems that generate more notifications, consider using a
                wrapping element so they can easily stack.
              </p>
              <div class="bg-dark p-3 mt-3">
                <div
                  aria-live="polite"
                  aria-atomic="true"
                  style="position: relative; min-height: 200px"
                >
                  <div style="position: absolute; top: 0; right: 0">
                    <toast class="fade show mb-2">
                      <toast-header>
                        <svg
                          class="bd-placeholder-img rounded me-2"
                          width="20"
                          height="20"
                          xmlns="http://www.w3.org/2000/svg"
                          preserveAspectRatio="xMidYMid slice"
                          focusable="false"
                          role="img"
                        >
                          <rect
                            width="100%"
                            height="100%"
                            fill="#007aff"
                          ></rect>
                        </svg>
                        <strong class="me-auto">Bootstrap</strong>
                        <small class="text-muted">just now</small>
                        <button
                          :dismissable="true"
                          type="button"
                          :class="`btn-close ms-2 mb-1 ${buttonClass}`"
                          data-bs-dismiss="toast"
                          aria-label="Close"
                        ></button>
                      </toast-header>
                      <toast-body> See? Just like this. </toast-body>
                    </toast>
                    <toast class="fade show">
                      <toast-header>
                        <svg
                          class="bd-placeholder-img rounded me-2"
                          width="20"
                          height="20"
                          xmlns="http://www.w3.org/2000/svg"
                          preserveAspectRatio="xMidYMid slice"
                          focusable="false"
                          role="img"
                        >
                          <rect
                            width="100%"
                            height="100%"
                            fill="#007aff"
                          ></rect>
                        </svg>
                        <strong class="me-auto">Bootstrap</strong>
                        <small class="text-muted">2 seconds ago</small>
                        <button
                          :dismissable="true"
                          type="button"
                          :class="`btn-close ms-2 mb-1 ${buttonClass}`"
                          data-bs-dismiss="toast"
                          aria-label="Close"
                        ></button>
                      </toast-header>
                      <toast-body>
                        Heads up, toasts will stack automatically
                      </toast-body>
                    </toast>
                  </div>
                </div>
              </div>
            </template>
          </iq-card>
        </b-col>
        <b-col sm="12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Notifications</h4>
            </template>

            <template v-slot:body>
              <p>
                Toasts are as flexible as you need and have very little required
                markup. At a minimum, we require a single element to contain
                your “toasted” content and strongly encourage a dismiss button.
              </p>

              <toast class="fade show bg-primary text-white border-0">
                <toast-header headerClass="bg-primary text-white">
                  <svg
                    class="bd-placeholder-img rounded me-2"
                    width="20"
                    height="20"
                    xmlns="http://www.w3.org/2000/svg"
                    preserveAspectRatio="xMidYMid slice"
                    focusable="false"
                    role="img"
                  >
                    <rect width="100%" height="100%" fill="#fff"></rect>
                  </svg>
                  <strong class="me-auto text-white">Bootstrap</strong>
                  <small>11 mins ago</small>
                  <button
                    :dismissable="true"
                    type="button"
                    class="btn-close ms-2 mb-1 btn-close-white text-white"
                    data-bs-dismiss="toast"
                    aria-label="Close"
                  ></button>
                </toast-header>
                <toast-body>
                  Hello, world! This is a toast message.
                </toast-body>
              </toast>
              <toast class="fade show bg-success text-white border-0 mt-3">
                <toast-header headerClass="bg-success text-white">
                  <svg
                    class="bd-placeholder-img rounded me-2"
                    width="20"
                    height="20"
                    xmlns="http://www.w3.org/2000/svg"
                    preserveAspectRatio="xMidYMid slice"
                    focusable="false"
                    role="img"
                  >
                    <rect width="100%" height="100%" fill="#fff"></rect>
                  </svg>
                  <strong class="me-auto text-white">Bootstrap</strong>
                  <small>11 mins ago</small>
                  <button
                    :dismissable="true"
                    type="button"
                    class="btn-close ms-2 mb-1 btn-close-white text-white"
                    data-bs-dismiss="toast"
                    aria-label="Close"
                  ></button>
                </toast-header>
                <toast-body>
                  Hello, world! This is a toast message.
                </toast-body>
              </toast>
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
  name: "UiNotifications",
  mounted() {
    // socialvue.index()
  },
};
</script>
