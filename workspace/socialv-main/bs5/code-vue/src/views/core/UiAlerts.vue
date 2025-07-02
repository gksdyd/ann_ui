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
              <h3 class="text-white">Alert Page</h3>
              <p class="text-white">lorem ipsum</p>
            </div>
          </b-card>
        </b-col>
        <b-col sm="12" lg="6">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Basic Alerts</h4>
            </template>
            <template v-slot:body>
              <p class="mb-4">
                Lorem Ipsum is simply dummy text of the printing and typesetting
                industry. Lorem Ipsum has been the industry's standard dummy
                text ever
              </p>
              <alert
                variant="success"
                :isdismissable="true"
                className="fade show mb-3"
              >
                <template v-slot>
                  <span class="d-flex"
                    ><i class="material-symbols-outlined me-2">thumb_up</i> This
                    is a success alert—check it out!</span
                  >
                  <!-- <span> This is a success alert—check it out!</span> -->
                </template>
              </alert>
              <alert
                variant="info"
                :isdismissable="true"
                className="fade show mb-3"
              >
                <template v-slot>
                  <span class="d-flex"
                    ><i class="material-symbols-outlined me-2">notifications</i
                    >This is a info alert—check it out!</span
                  >
                </template>
              </alert>
              <alert
                variant="warning"
                :isdismissable="true"
                className="fade show mb-3"
              >
                <template v-slot>
                  <span class="d-flex"
                    ><i class="material-symbols-outlined me-2">notifications</i>
                    This is a warning alert—check it out!</span
                  >
                </template>
              </alert>
              <alert
                variant="danger"
                :isdismissable="true"
                className="fade show"
              >
                <template v-slot>
                  <span class="d-flex"
                    ><i class="material-symbols-outlined me-2">rotate_right</i>
                    This is a danger alert—check it out!</span
                  >
                </template>
              </alert>
            </template>
          </iq-card>
        </b-col>
        <b-col sm="12" lg="6">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Basic Alerts With Icons</h4>
            </template>

            <template v-slot:body>
              <svg xmlns="http://www.w3.org/2000/svg" style="display: none">
                <symbol
                  id="check-circle-fill"
                  fill="currentColor"
                  viewBox="0 0 16 16"
                >
                  <path
                    d="M16 8A8 8 0 1 1 0 8a8 8 0 0 1 16 0zm-3.97-3.03a.75.75 0 0 0-1.08.022L7.477 9.417 5.384 7.323a.75.75 0 0 0-1.06 1.06L6.97 11.03a.75.75 0 0 0 1.079-.02l3.992-4.99a.75.75 0 0 0-.01-1.05z"
                  />
                </symbol>
                <symbol id="info-fill" fill="currentColor" viewBox="0 0 16 16">
                  <path
                    d="M8 16A8 8 0 1 0 8 0a8 8 0 0 0 0 16zm.93-9.412-1 4.705c-.07.34.029.533.304.533.194 0 .487-.07.686-.246l-.088.416c-.287.346-.92.598-1.465.598-.703 0-1.002-.422-.808-1.319l.738-3.468c.064-.293.006-.399-.287-.47l-.451-.081.082-.381 2.29-.287zM8 5.5a1 1 0 1 1 0-2 1 1 0 0 1 0 2z"
                  />
                </symbol>
                <symbol
                  id="exclamation-triangle-fill"
                  fill="currentColor"
                  viewBox="0 0 16 16"
                >
                  <path
                    d="M8.982 1.566a1.13 1.13 0 0 0-1.96 0L.165 13.233c-.457.778.091 1.767.98 1.767h13.713c.889 0 1.438-.99.98-1.767L8.982 1.566zM8 5c.535 0 .954.462.9.995l-.35 3.507a.552.552 0 0 1-1.1 0L7.1 5.995A.905.905 0 0 1 8 5zm.002 6a1 1 0 1 1 0 2 1 1 0 0 1 0-2z"
                  />
                </symbol>
              </svg>

              <alert variant="primary" className="d-flex align-items-center">
                <template v-slot>
                  <svg class="bi flex-shrink-0 me-2" width="24" height="24">
                    <use xlink:href="#info-fill" />
                  </svg>
                  <div>An example alert with an icon</div>
                </template>
              </alert>
              <alert
                :show="true"
                variant="success"
                className="d-flex align-items-center"
              >
                <template v-slot>
                  <svg class="bi flex-shrink-0 me-2" width="24" height="24">
                    <use xlink:href="#exclamation-triangle-fill" />
                  </svg>
                  <div>An example success alert with an icon</div>
                </template>
              </alert>
              <alert
                :show="true"
                variant="warning"
                className="d-flex align-items-center"
              >
                <template v-slot>
                  <svg class="bi flex-shrink-0 me-2" width="24" height="24">
                    <use xlink:href="#exclamation-triangle-fill" />
                  </svg>
                  <div>An example warning alert with an icon</div>
                </template>
              </alert>
              <alert
                :show="true"
                variant="danger"
                className="d-flex align-items-center"
              >
                <template v-slot>
                  <svg class="bi flex-shrink-0 me-2" width="24" height="24">
                    <use xlink:href="#exclamation-triangle-fill" />
                  </svg>
                  <div>An example danger alert with an icon</div>
                </template>
              </alert>
            </template>
          </iq-card>
        </b-col>
      </b-row>
      <b-row>
        <b-col sm="12" lg="6">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Basic Line Alerts</h4>
            </template>

            <template v-slot:body>
              <alert
                variant="primary"
                :isdismissable="true"
                className="d-flex align-items-center alert-solid"
              >
                <template v-slot>
                  <span class="d-flex"
                    ><i class="material-symbols-outlined me-2">thumb_up</i>This
                    is a primary alert—check it out!</span
                  >
                </template>
              </alert>
              <alert
                variant="info"
                :isdismissable="true"
                className="fade show alert-solid mb-3"
              >
                <template v-slot>
                  <span class="d-flex"
                    ><i class="material-symbols-outlined me-2">notifications</i>
                    This is a info alert—check it out!</span
                  >
                </template>
              </alert>
              <alert
                variant="secondary"
                :isdismissable="true"
                className="fade show alert-solid mb-3"
              >
                <template v-slot>
                  <span class="d-flex"
                    ><i class="material-symbols-outlined me-2">notifications</i
                    >This is a secondary alert—check it out!</span
                  >
                </template>
              </alert>
              <alert
                variant="danger"
                :isdismissable="true"
                className="fade show alert-solid mb-3"
              >
                <template v-slot>
                  <span class="d-flex"
                    ><i class="material-symbols-outlined me-2">rotate_right</i>
                    This is a danger alert—check it out!</span
                  >
                </template>
              </alert>
            </template>
          </iq-card>
        </b-col>
        <b-col sm="12" lg="6">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Basic Line Alerts With Icons</h4>
            </template>

            <template v-slot:body>
              <svg xmlns="http://www.w3.org/2000/svg" style="display: none">
                <symbol
                  id="check-circle-fill"
                  fill="currentColor"
                  viewBox="0 0 16 16"
                >
                  <path
                    d="M16 8A8 8 0 1 1 0 8a8 8 0 0 1 16 0zm-3.97-3.03a.75.75 0 0 0-1.08.022L7.477 9.417 5.384 7.323a.75.75 0 0 0-1.06 1.06L6.97 11.03a.75.75 0 0 0 1.079-.02l3.992-4.99a.75.75 0 0 0-.01-1.05z"
                  />
                </symbol>
                <symbol id="info-fill" fill="currentColor" viewBox="0 0 16 16">
                  <path
                    d="M8 16A8 8 0 1 0 8 0a8 8 0 0 0 0 16zm.93-9.412-1 4.705c-.07.34.029.533.304.533.194 0 .487-.07.686-.246l-.088.416c-.287.346-.92.598-1.465.598-.703 0-1.002-.422-.808-1.319l.738-3.468c.064-.293.006-.399-.287-.47l-.451-.081.082-.381 2.29-.287zM8 5.5a1 1 0 1 1 0-2 1 1 0 0 1 0 2z"
                  />
                </symbol>
                <symbol
                  id="exclamation-triangle-fill"
                  fill="currentColor"
                  viewBox="0 0 16 16"
                >
                  <path
                    d="M8.982 1.566a1.13 1.13 0 0 0-1.96 0L.165 13.233c-.457.778.091 1.767.98 1.767h13.713c.889 0 1.438-.99.98-1.767L8.982 1.566zM8 5c.535 0 .954.462.9.995l-.35 3.507a.552.552 0 0 1-1.1 0L7.1 5.995A.905.905 0 0 1 8 5zm.002 6a1 1 0 1 1 0 2 1 1 0 0 1 0-2z"
                  />
                </symbol>
              </svg>
              <alert
                variant="primary"
                className="d-flex align-items-center alert-solid"
              >
                <template v-slot>
                  <svg class="bi flex-shrink-0 me-2" width="24" height="24">
                    <use xlink:href="#info-fill" />
                  </svg>
                  <div>An example alert alert-solid with an icon</div>
                </template>
              </alert>
              <alert
                variant="success"
                className="d-flex align-items-center alert-solid"
              >
                <template v-slot>
                  <svg class="bi flex-shrink-0 me-2" width="24" height="24">
                    <use xlink:href="#exclamation-triangle-fill" />
                  </svg>
                  <div>An example success alert alert-solid with an icon</div>
                </template>
              </alert>
              <alert
                variant="warning"
                className="d-flex align-items-center alert-solid"
              >
                <template v-slot>
                  <svg class="bi flex-shrink-0 me-2" width="24" height="24">
                    <use xlink:href="#exclamation-triangle-fill" />
                  </svg>
                  <div>An example warning alert alert-solid with an icon</div>
                </template>
              </alert>
              <alert
                variant="danger"
                className="d-flex align-items-center alert-solid"
              >
                <template v-slot>
                  <svg class="bi flex-shrink-0 me-2" width="24" height="24">
                    <use xlink:href="#exclamation-triangle-fill" />
                  </svg>
                  <div>An example danger alert alert-solid with an icon</div>
                </template>
              </alert>
            </template>
          </iq-card>
        </b-col>
      </b-row>
      <b-row>
        <b-col md="12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Alerts With Background</h4>
            </template>
            <template v-slot:body>
              <alert
                variant="success"
                :isdismissable="true"
                className="fade show alert-left mb-3"
              >
                <template v-slot>
                  <span class="d-flex"
                    ><i class="material-symbols-outlined me-2">thumb_up</i>This
                    is a success alert—check it out!</span
                  >
                </template>
              </alert>
              <alert
                variant="warning"
                :isdismissable="true"
                className="fade show alert-top mb-3"
              >
                <template v-slot>
                  <span class="d-flex"
                    ><i class="material-symbols-outlined me-2">notifications</i>
                    This is a warning alert—check it out!</span
                  >
                </template>
              </alert>
              <alert
                variant="secondary"
                :isdismissable="true"
                className="fade show alert-right mb-3"
              >
                <template v-slot>
                  <span class="d-flex"
                    ><i class="material-symbols-outlined me-2">notifications</i>
                    <span> This is a secondary alert—check it out!</span>
                  </span>
                </template>
              </alert>
              <alert
                variant="danger"
                :isdismissable="true"
                className="fade show alert-bottom mb-3"
              >
                <template v-slot>
                  <span class="d-flex"
                    ><i class="material-symbols-outlined me-2">rotate_right</i>
                    This is a danger alert—check it out!</span
                  >
                </template>
              </alert>
            </template>
          </iq-card>
        </b-col>
        <b-col md="12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">For Banner</h4>
            </template>
            <template v-slot:body>
              <alert
                variant="success"
                :isdismissable="true"
                className="fade show rounded-0 mb-3"
              >
                <template v-slot>
                  <span class="d-flex"
                    ><i class="material-symbols-outlined me-2">rotate_right</i>
                    This is a success alert—check it out!</span
                  >
                </template>
              </alert>
              <alert
                variant="warning"
                :isdismissable="true"
                className="fade show rounded-0 alert-solid mb-3"
                buttonClass="btn-close"
              >
                <template v-slot>
                  <span class="d-flex"
                    ><i class="material-symbols-outlined me-2">rotate_right</i>
                    This is a warning alert—check it out!</span
                  >
                </template>
              </alert>
            </template>
          </iq-card>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>
<script>
export default {
  name: "UiAlerts",
};
</script>
