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
              <h3 class="text-white">Button Page</h3>
              <p class="text-white">lorem ipsum</p>
            </div>
          </b-card>
        </b-col>
        <b-col lg="6" sm="12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Default Buttons</h4>
            </template>
            <template v-slot:body>
              <p class="mb-4">
                Lorem Ipsum is simply dummy text of the printing and typesetting
                industry. Lorem Ipsum has been the industry's standard dummy
                text ever
              </p>
              <button type="button" class="btn btn-primary mb-3 me-1">
                Primary
              </button>
              {{ "" }}
              <button type="button" class="btn btn-secondary mb-3 me-1">
                Secondary
              </button>
              {{ "" }}
              <button type="button" class="btn btn-success mb-3 me-1">
                Success
              </button>
              {{ "" }}
              <button type="button" class="btn btn-danger mb-3 me-1">
                Danger
              </button>
              {{ "" }}
              <button type="button" class="btn btn-warning mb-3 me-1">
                Warning
              </button>
              {{ "" }}
              <button type="button" class="btn btn-info mb-3 me-1">Info</button>
              {{ "" }}
              <button type="button" class="btn btn-light mb-3 me-1">
                Light
              </button>
              {{ "" }}
              <button type="button" class="btn btn-dark mb-3 me-1">Dark</button>
              {{ "" }}
              <button type="button" class="btn btn-link mb-3 me-1">Link</button>
            </template>
          </iq-card>
        </b-col>
        <b-col lg="6" sm="12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Default Buttons Rounded Shape</h4>
            </template>
            <template v-slot:body>
              <p class="mb-4">
                Lorem Ipsum is simply dummy text of the printing and typesetting
                industry. Lorem Ipsum has been the industry's standard dummy
                text ever
              </p>
              <button
                type="button"
                class="btn btn-primary rounded-pill mb-3 me-1"
              >
                Primary
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-secondary rounded-pill mb-3 me-1"
              >
                Secondary
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-success rounded-pill mb-3 me-1"
              >
                Success
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-danger rounded-pill mb-3 me-1"
              >
                Danger
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-warning rounded-pill mb-3 me-1"
              >
                Warning
              </button>
              {{ "" }}
              <button type="button" class="btn btn-info rounded-pill mb-3 me-1">
                Info
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-light rounded-pill mb-3 me-1"
              >
                Light
              </button>
              {{ "" }}
              <button type="button" class="btn btn-dark rounded-pill mb-3 me-1">
                Dark
              </button>
              {{ "" }}
              <button type="button" class="btn btn-link rounded-pill mb-3 me-1">
                Link
              </button>
            </template>
          </iq-card>
        </b-col>
      </b-row>
      <b-row>
        <b-col lg="6" sm="12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Outline Buttons</h4>
            </template>
            <template v-slot:body>
              <p class="mb-4">
                Lorem Ipsum is simply dummy text of the printing and typesetting
                industry. Lorem Ipsum has been the industry's standard dummy
                text ever
              </p>
              <button type="button" class="btn btn-outline-primary mb-3 me-1">
                Primary
              </button>
              {{ "" }}
              <button type="button" class="btn btn-outline-secondary mb-3 me-1">
                Secondary
              </button>
              {{ "" }}
              <button type="button" class="btn btn-outline-success mb-3 me-1">
                Success
              </button>
              {{ "" }}
              <button type="button" class="btn btn-outline-danger mb-3 me-1">
                Danger
              </button>
              {{ "" }}
              <button type="button" class="btn btn-outline-warning mb-3 me-1">
                Warning
              </button>
              {{ "" }}
              <button type="button" class="btn btn-outline-info mb-3 me-1">
                Info
              </button>
              {{ "" }}
              <button type="button" class="btn btn-outline-dark mb-3 me-1">
                Dark
              </button>
            </template>
          </iq-card>
        </b-col>
        <b-col lg="6" sm="12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Rounded Outline Buttons</h4>
            </template>
            <template v-slot:body>
              <p class="mb-4">
                Lorem Ipsum is simply dummy text of the printing and typesetting
                industry. Lorem Ipsum has been the industry's standard dummy
                text ever
              </p>
              <button
                type="button"
                class="btn btn-outline-primary rounded-pill mb-3 me-1"
              >
                Primary
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-outline-secondary rounded-pill mb-3 me-1"
              >
                Secondary
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-outline-success rounded-pill mb-3 me-1"
              >
                Success
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-outline-danger rounded-pill mb-3 me-1"
              >
                Danger
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-outline-warning rounded-pill mb-3 me-1"
              >
                Warning
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-outline-info rounded-pill mb-3 me-1"
              >
                Info
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-outline-dark rounded-pill mb-3 me-1"
              >
                Dark
              </button>
            </template>
          </iq-card>
        </b-col>
      </b-row>
      <b-row>
        <b-col sm="12" lg="6">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Soft Buttons</h4>
            </template>
            <template v-slot:body>
              <p class="mb-4">
                Lorem Ipsum is simply dummy text of the printing and typesetting
                industry. Lorem Ipsum has been the industry's standard dummy
                text ever
              </p>
              <b-button variant="primary-subtle" class="mb-3 me-1"
                >Primary</b-button
              >
              {{ "" }}
              <b-button variant="secondary-subtle" class="mb-3 me-1"
                >Secondary</b-button
              >
              {{ "" }}
              <b-button variant="success-subtle" class="mb-3 me-1"
                >Success</b-button
              >
              {{ "" }}
              <b-button variant="danger-subtle" class="mb-3 me-1"
                >Danger</b-button
              >
              {{ "" }}
              <b-button variant="warning-subtle" class="mb-3 me-1"
                >Warning</b-button
              >
              {{ "" }}
              <b-button variant="info-subtle" class="mb-3 me-1">Info</b-button>
              {{ "" }}
              <b-button variant="dark-subtle" class="mb-3 me-1">Dark</b-button>
              {{ "" }}
              <b-button variant="gray-subtle" class="mb-3 me-1">Link</b-button>
            </template>
          </iq-card>
        </b-col>
        <b-col sm="12" lg="6">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Rounded Soft Buttons</h4>
            </template>
            <template v-slot:body>
              <p class="mb-4">
                Lorem Ipsum is simply dummy text of the printing and typesetting
                industry. Lorem Ipsum has been the industry's standard dummy
                text ever
              </p>
              <b-button variant="primary-subtle" class="mb-3 me-1" rounded pill
                >Primary</b-button
              >
              {{ "" }}
              <b-button
                variant="secondary-subtle"
                class="mb-3 me-1"
                rounded
                pill
                >Secondary</b-button
              >
              {{ "" }}
              <b-button variant="success-subtle" class="mb-3 me-1" rounded pill
                >Success</b-button
              >
              {{ "" }}
              <b-button variant="danger-subtle" class="mb-3 me-1" rounded pill
                >Danger</b-button
              >
              {{ "" }}
              <b-button variant="warning-subtle" class="mb-3 me-1" rounded pill
                >Warning</b-button
              >
              {{ "" }}
              <b-button variant="info-subtle" class="mb-3 me-1" rounded pill
                >Info</b-button
              >
              {{ "" }}
              <b-button variant="dark-subtle" class="mb-3 me-1" rounded pill
                >Dark</b-button
              >
              {{ "" }}
              <b-button variant="gray-subtle" class="mb-3 me-1" rounded pill
                >Link</b-button
              >
            </template>
          </iq-card>
        </b-col>
      </b-row>
      <b-row>
        <b-col lg="6" sm="12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Default Buttons</h4>
            </template>
            <template v-slot:body>
              <p class="mb-4">
                Lorem Ipsum is simply dummy text of the printing and typesetting
                industry. Lorem Ipsum has been the industry's standard dummy
                text ever
              </p>
              <button
                type="button"
                class="btn btn-primary d-inline-flex mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">subject</i>Primary
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-secondary d-inline-flex mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">favorite</i>Secondary
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-success d-inline-flex mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">subject</i>Success
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-danger d-inline-flex mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">favorite</i>Danger
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-warning d-inline-flex mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">subject</i>Warning
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-info d-inline-flex mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">favorite</i>Info
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-light d-inline-flex mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">subject</i>Light
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-dark d-inline-flex mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">favorite</i>Dark
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-link d-inline-flex mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">subject</i>Link
              </button>
            </template>
          </iq-card>
        </b-col>
        <b-col lg="6" sm="12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Default Buttons Rounded Shape</h4>
            </template>
            <template v-slot:body>
              <p class="mb-4">
                Lorem Ipsum is simply dummy text of the printing and typesetting
                industry. Lorem Ipsum has been the industry's standard dummy
                text ever
              </p>
              <button
                type="button"
                class="btn btn-primary d-inline-flex rounded-pill mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">subject</i>Primary
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-secondary d-inline-flex rounded-pill mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">favorite</i>Secondary
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-success d-inline-flex rounded-pill mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">subject</i>Success
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-danger d-inline-flex rounded-pill mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">favorite</i>Danger
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-warning d-inline-flex rounded-pill mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">subject</i>Warning
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-info d-inline-flex rounded-pill mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">favorite</i>Info
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-light d-inline-flex rounded-pill mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">subject</i>Light
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-dark d-inline-flex rounded-pill mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">favorite</i>Dark
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-link d-inline-flex rounded-pill mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">subject</i>Link
              </button>
            </template>
          </iq-card>
        </b-col>
      </b-row>
      <b-row>
        <b-col lg="6" sm="12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Outline Buttons</h4>
            </template>
            <template v-slot:body>
              <p class="mb-4">
                Lorem Ipsum is simply dummy text of the printing and typesetting
                industry. Lorem Ipsum has been the industry's standard dummy
                text ever
              </p>
              <button
                type="button"
                class="btn btn-outline-primary d-inline-flex mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">favorite</i>Primary
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-outline-secondary d-inline-flex mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">warning</i>Secondary
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-outline-success d-inline-flex mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">favorite</i>Success
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-outline-danger d-inline-flex mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">warning</i>Danger
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-outline-warning d-inline-flex mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">favorite</i>Warning
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-outline-info d-inline-flex mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">warning</i>Info
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-outline-dark d-inline-flex mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">warning</i>Dark
              </button>
            </template>
          </iq-card>
        </b-col>
        <b-col lg="6" sm="12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Rounded Outline Buttons</h4>
            </template>
            <template v-slot:body>
              <p class="mb-4">
                Lorem Ipsum is simply dummy text of the printing and typesetting
                industry. Lorem Ipsum has been the industry's standard dummy
                text ever
              </p>
              <button
                type="button"
                class="btn btn-outline-primary rounded-pill d-inline-flex mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">favorite</i>Primary
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-outline-secondary rounded-pill d-inline-flex mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">warning</i>Secondary
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-outline-success rounded-pill d-inline-flex mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">favorite</i>Success
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-outline-danger rounded-pill d-inline-flex mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">warning</i>Danger
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-outline-warning rounded-pill d-inline-flex mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">favorite</i>Warning
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-outline-info rounded-pill d-inline-flex mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">warning</i>Info
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-outline-dark rounded-pill d-inline-flex mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">warning</i>Dark
              </button>
            </template>
          </iq-card>
        </b-col>
      </b-row>
      <b-row>
        <b-col lg="6" sm="12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Outline Buttons</h4>
            </template>
            <template v-slot:body>
              <p class="mb-4">
                Lorem Ipsum is simply dummy text of the printing and typesetting
                industry. Lorem Ipsum has been the industry's standard dummy
                text ever
              </p>
              <button
                type="button"
                class="btn btn-primary-subtle d-inline-flex mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">favorite</i>Primary
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-secondary-subtle d-inline-flex mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">warning</i>Secondary
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-success-subtle d-inline-flex mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">favorite</i>Success
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-danger-subtle d-inline-flex mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">warning</i>Danger
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-warning-subtle d-inline-flex mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">favorite</i>Warning
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-info-subtle d-inline-flex mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">warning</i>Info
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-dark-subtle d-inline-flex mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">warning</i>Dark
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-gray-subtle d-inline-flex mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">favorite</i>Link
              </button>
            </template>
          </iq-card>
        </b-col>
        <b-col lg="6" sm="12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Rounded Outline Buttons</h4>
            </template>
            <template v-slot:body>
              <p class="mb-4">
                Lorem Ipsum is simply dummy text of the printing and typesetting
                industry. Lorem Ipsum has been the industry's standard dummy
                text ever
              </p>
              <button
                type="button"
                class="btn btn-primary-subtle rounded-pill d-inline-flex mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">favorite</i>Primary
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-secondary-subtle rounded-pill d-inline-flex mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">warning</i>Secondary
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-success-subtle rounded-pill d-inline-flex mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">favorite</i>Success
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-danger-subtle rounded-pill d-inline-flex mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">warning</i>Danger
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-warning-subtle rounded-pill d-inline-flex mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">favorite</i>Warning
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-info-subtle rounded-pill d-inline-flex mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">warning</i>Info
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-dark-subtle rounded-pill d-inline-flex mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">warning</i>Dark
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-gray-subtle rounded-pill d-inline-flex mb-3 me-1"
              >
                <i class="material-symbols-outlined me-1">favorite</i>Link
              </button>
            </template>
          </iq-card>
        </b-col>
      </b-row>
      <b-row>
        <b-col lg="6" sm="12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Button Tags</h4>
            </template>
            <template v-slot:body>
              <p class="mb-3">
                Lorem Ipsum is simply dummy text of the printing and typesetting
                industry. Lorem Ipsum has been the industry's standard dummy
                text ever
              </p>
              <button type="button" class="btn mt-1 btn-primary">Link</button>
              {{ "" }}
              <button type="button" class="btn mt-1 btn-success">Button</button>
              {{ "" }}
              <button type="button" class="btn mt-1 btn-danger">Input</button>
              {{ "" }}
              <button type="button" class="btn mt-1 btn-warning">Submit</button>
              {{ "" }}
              <button type="button" class="btn mt-1 btn-info">Reset</button>
            </template>
          </iq-card>
        </b-col>
        <b-col lg="6" sm="12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Buttons Sizes</h4>
            </template>
            <template v-slot:body>
              <p class="mb-3">
                Lorem Ipsum is simply dummy text of the printing and typesetting
                industry. Lorem Ipsum has been the industry's standard dummy
                text ever
              </p>
              <button type="button" class="btn btn-primary mt-1 btn-sm">
                Small button
              </button>
              {{ "" }}
              <button type="button" class="btn btn-success mt-1">Button</button>
              {{ "" }}
              <button type="button" class="btn btn-info mt-1 btn-lg">
                Large Button
              </button>
            </template>
          </iq-card>
        </b-col>
      </b-row>
      <b-row>
        <b-col lg="6" sm="12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Block Buttons</h4>
            </template>
            <template v-slot:body>
              <p class="mb-3">
                Lorem Ipsum is simply dummy text of the printing and typesetting
                industry. Lorem Ipsum has been the industry's standard dummy
                text ever
              </p>
              <!-- <b-button block variant="primary">Block level button</b-button>
              <b-button block variant="success">Block level button</b-button> -->
              <div class="d-grid gap-2">
                <button class="btn btn-primary" type="button">
                  Block level Button
                </button>
                <button class="btn btn-success" type="button">
                  Block level Button
                </button>
              </div>
            </template>
          </iq-card>
        </b-col>
        <b-col lg="6" sm="12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Icons Buttons</h4>
            </template>
            <template v-slot:body>
              <p class="mb-4">
                Lorem Ipsum is simply dummy text of the printing and typesetting
                industry. Lorem Ipsum has been the industry's standard dummy
                text ever
              </p>
              <button
                type="button"
                class="btn d-inline-flex btn-primary me-1 mb-1"
              >
                <i class="material-symbols-outlined me-0">info</i>
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn d-inline-flex btn-secondary me-1 mb-1"
              >
                <i class="material-symbols-outlined me-0">gpp_maybe</i>
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn d-inline-flex btn-success me-1 mb-1"
              >
                <i class="material-symbols-outlined me-0">add_alert</i>
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn d-inline-flex btn-danger me-1 mb-1"
              >
                <i class="material-symbols-outlined me-0">report_off</i>
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn d-inline-flex btn-warning me-1 mb-1"
              >
                <i class="material-symbols-outlined me-0">show_chart</i>
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn d-inline-flex btn-info me-1 mb-1"
              >
                <i class="material-symbols-outlined me-0">wifi_off</i>
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn d-inline-flex btn-light me-1 mb-1"
              >
                <i class="material-symbols-outlined me-0">rss_feed</i>
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn d-inline-flex btn-dark me-1 mb-1"
              >
                <i class="material-symbols-outlined me-0">backup</i>
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn d-inline-flex btn-link me-1 mb-1"
              >
                <i class="material-symbols-outlined me-0">album</i>
              </button>
              {{ "" }}
              <div class="d-inline-block w-100 mt-1">
                <button
                  type="button"
                  class="btn d-inline-flex btn-primary me-1 mb-1"
                >
                  <i class="material-symbols-outlined me-1">favorite</i>Buttons
                </button>
                {{ "" }}
                <button
                  type="button"
                  class="btn d-inline-flex btn-secondary me-1 mb-1"
                >
                  <i class="material-symbols-outlined me-1">favorite</i>Buttons
                </button>
                {{ "" }}
                <button
                  type="button"
                  class="btn d-inline-flex btn-success me-1 mb-1"
                >
                  <i class="material-symbols-outlined me-1">favorite</i>Buttons
                </button>
                {{ "" }}
                <button
                  type="button"
                  class="btn d-inline-flex btn-danger me-1 mb-1"
                >
                  <i class="material-symbols-outlined me-1">favorite</i>Buttons
                </button>
                {{ "" }}
                <button
                  type="button"
                  class="btn d-inline-flex btn-info me-1 mb-1"
                >
                  <i class="material-symbols-outlined me-1">favorite</i>Buttons
                </button>
              </div>
            </template>
          </iq-card>
        </b-col>
      </b-row>
      <b-row>
        <b-col lg="6" sm="12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Social Disabled State</h4>
            </template>
            <template v-slot:body>
              <p class="mb-4">
                Lorem Ipsum is simply dummy text of the printing and typesetting
                industry. Lorem Ipsum has been the industry's standard dummy
                text ever
              </p>
              <button type="button" class="btn btn-primary" disabled="">
                Primary button
              </button>
              {{ "" }}
              <button
                type="button"
                disabled="disabled"
                class="btn btn-success disabled"
              >
                Button
              </button>
              {{ "" }}
              <button
                type="button"
                disabled="disabled"
                class="btn btn-outline-primary disabled"
              >
                Button
              </button>
            </template>
          </iq-card>
        </b-col>
        <b-col lg="6" sm="12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Buttons Toggle States</h4>
            </template>
            <template v-slot:body>
              <p class="mb-4">
                Lorem Ipsum is simply dummy text of the printing and typesetting
                industry. Lorem Ipsum has been the industry's standard dummy
                text ever
              </p>
              <button
                type="button"
                class="btn btn-primary"
                data-toggle="button"
                aria-pressed="false"
              >
                Single toggle
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-primary active"
                data-toggle="button"
                aria-pressed="false"
              >
                Single toggle
              </button>
              {{ "" }}
              <button
                type="button"
                class="btn btn-primary disabled"
                data-toggle="button"
                aria-pressed="false"
              >
                Single toggle
              </button>
            </template>
          </iq-card>
        </b-col>
      </b-row>
      <b-row>
        <b-col lg="6" sm="12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Default Buttons Active</h4>
            </template>
            <template v-slot:body>
              <p class="mb-4">
                Lorem Ipsum is simply dummy text of the printing and typesetting
                industry. Lorem Ipsum has been the industry's standard dummy
                text ever
              </p>
              <button type="button" class="btn btn-primary active mb-1">
                Active
              </button>
              {{ "" }}
              <button type="button" class="btn active mb-1 btn-secondary">
                Active
              </button>
              {{ "" }}
              <button type="button" class="btn active mb-1 btn-warning">
                Active
              </button>
              {{ "" }}
              <button
                type="button"
                disabled="disabled"
                class="btn mb-1 btn-accent disabled"
              >
                Disabled
              </button>
              {{ "" }}
              <button
                type="button"
                disabled="disabled"
                class="btn mb-1 btn-primary disabled"
              >
                Disabled
              </button>
              {{ "" }}
              <button
                type="button"
                disabled="disabled"
                class="btn mb-1 btn-outline-primary disabled"
              >
                Disabled
              </button>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Button Group Sizing</h4>
            </template>
            <template v-slot:body>
              <p class="mb-4">
                Lorem Ipsum is simply dummy text of the printing and typesetting
                industry. Lorem Ipsum has been the industry's standard dummy
                text ever
              </p>
              <div class="bd-example">
                <div
                  class="btn-group btn-group-lg"
                  role="group"
                  aria-label="Large button group"
                >
                  <button type="button" class="btn btn-outline-primary">
                    Left
                  </button>
                  <button type="button" class="btn btn-outline-primary">
                    Middle
                  </button>
                  <button type="button" class="btn btn-outline-primary">
                    Right
                  </button>
                </div>
                {{ "" }}
                <br />
                <div
                  class="btn-group"
                  role="group"
                  aria-label="Default button group"
                >
                  <button type="button" class="btn btn-outline-primary">
                    Left
                  </button>
                  <button type="button" class="btn btn-outline-primary">
                    Middle
                  </button>
                  <button type="button" class="btn btn-outline-primary">
                    Right
                  </button>
                </div>
                {{ "" }}
                <br />
                <div
                  class="btn-group btn-group-sm"
                  role="group"
                  aria-label="Small button group"
                >
                  <button type="button" class="btn btn-outline-primary">
                    Left
                  </button>
                  <button type="button" class="btn btn-outline-primary">
                    Middle
                  </button>
                  <button type="button" class="btn btn-outline-primary">
                    Right
                  </button>
                </div>
              </div>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Button Group Vertical</h4>
            </template>
            <template v-slot:body>
              <p class="mb-4">
                Lorem Ipsum is simply dummy text of the printing and typesetting
                industry. Lorem Ipsum has been the industry's standard dummy
                text ever
              </p>
              <div
                class="btn-group-vertical"
                role="group"
                aria-label="Vertical radio toggle button group"
              >
                <input
                  id="vbtn-radio1"
                  type="radio"
                  class="btn-check"
                  name="vbtn-radio"
                  checked
                />
                <label class="btn btn-outline-danger" for="vbtn-radio1"
                  >Radio 1</label
                >
                <input
                  id="vbtn-radio2"
                  type="radio"
                  class="btn-check"
                  name="vbtn-radio"
                />
                <label class="btn btn-outline-danger" for="vbtn-radio2"
                  >Radio 2</label
                >
                <input
                  id="vbtn-radio3"
                  type="radio"
                  class="btn-check"
                  name="vbtn-radio"
                />
                <label class="btn btn-outline-danger" for="vbtn-radio3"
                  >Radio 3</label
                >
              </div>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Checkbox and radio button groups</h4>
            </template>
            <template v-slot:body>
              <p class="mb-4">
                Lorem Ipsum is simply dummy text of the printing and typesetting
                industry. Lorem Ipsum has been the industry's standard dummy
                text ever
              </p>
              <div
                class="btn-group checkboxradio me-1"
                role="group"
                aria-label="Basic checkbox toggle button group"
              >
                <input id="btncheck1" type="checkbox" class="btn-check" />
                <label class="btn btn-outline-primary" for="btncheck1"
                  >Checkbox 1</label
                >
                <input id="btncheck2" type="checkbox" class="btn-check" />
                <label class="btn btn-outline-primary" for="btncheck2"
                  >Checkbox 2</label
                >
                <input id="btncheck3" type="checkbox" class="btn-check" />
                <label class="btn btn-outline-primary" for="btncheck3"
                  >Checkbox 3</label
                >
              </div>
              <div
                class="btn-group mt-xl-1 checkboxradio"
                role="group"
                aria-label="Basic radio toggle button group"
              >
                <input
                  id="btnradio1"
                  type="radio"
                  class="btn-check"
                  name="btnradio"
                  checked
                />
                <label class="btn btn-outline-primary" for="btnradio1"
                  >Radio 1</label
                >
                <input
                  id="btnradio2"
                  type="radio"
                  class="btn-check"
                  name="btnradio"
                />
                <label class="btn btn-outline-primary" for="btnradio2"
                  >Radio 2</label
                >
                <input
                  id="btnradio3"
                  type="radio"
                  class="btn-check"
                  name="btnradio"
                />
                <label class="btn btn-outline-primary" for="btnradio3"
                  >Radio 3</label
                >
              </div>
            </template>
          </iq-card>
        </b-col>
        <b-col lg="6" sm="12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Button Group</h4>
            </template>
            <template v-slot:body>
              <p class="mb-3">
                Lorem Ipsum is simply dummy text of the printing and typesetting
                industry. Lorem Ipsum has been the industry's standard dummy
                text ever
              </p>
              <div
                class="btn-group mt-1"
                role="group"
                aria-label="Basic example"
              >
                <button type="button" class="btn btn-primary">Left</button>
                <button type="button" class="btn btn-primary">Middle</button>
                <button type="button" class="btn btn-primary">Right</button>
              </div>
              {{ "" }}
              <div class="btn-group mt-1 me-1">
                <a href="#" class="btn btn-primary active" aria-current="page"
                  >Active link</a
                >
                <a href="#" class="btn btn-primary">Link</a>
                <a href="#" class="btn btn-primary">Link</a>
              </div>
              <div
                class="btn-group mt-1"
                role="group"
                aria-label="Basic outlined example"
              >
                <button type="button" class="btn btn-outline-primary">
                  Left
                </button>
                <button type="button" class="btn btn-outline-primary">
                  Middle
                </button>
                <button type="button" class="btn btn-outline-primary">
                  Right
                </button>
              </div>
              {{ "" }}
              <div
                class="btn-group mt-1"
                role="group"
                aria-label="Basic mixed styles example"
              >
                <button type="button" class="btn btn-danger">Left</button>
                <button type="button" class="btn btn-warning">Middle</button>
                <button type="button" class="btn btn-success">Right</button>
              </div>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Button Dropdown</h4>
            </template>
            <template v-slot:body>
              <p class="mb-4">
                Lorem Ipsum is simply dummy text of the printing and typesetting
                industry. Lorem Ipsum has been the industry's standard dummy
                text ever
              </p>
              <div
                class="btn-group"
                role="group"
                aria-label="Button group with nested dropdown"
              >
                <button type="button" class="btn btn-primary">1</button>
                <button type="button" class="btn btn-primary">2</button>

                <div class="btn-group" role="group">
                  <button
                    id="btnGroupDrop1"
                    type="button"
                    class="btn btn-primary dropdown-toggle"
                    data-bs-toggle="dropdown"
                    aria-expanded="false"
                  >
                    Dropdown
                  </button>
                  <ul class="dropdown-menu" aria-labelledby="btnGroupDrop1">
                    <li><a class="dropdown-item" href="#">Dropdown link</a></li>
                    <li><a class="dropdown-item" href="#">Dropdown link</a></li>
                  </ul>
                </div>
              </div>
              <div class="d-block mt-1">
                <div
                  class="btn-group-vertical"
                  role="group"
                  aria-label="Vertical button group"
                >
                  <button type="button" class="btn btn-primary">Button</button>
                  <button type="button" class="btn btn-primary">Button</button>
                  <div class="btn-group" role="group">
                    <button
                      id="btnGroupVerticalDrop1"
                      type="button"
                      class="btn btn-primary dropdown-toggle"
                      data-bs-toggle="dropdown"
                      aria-expanded="false"
                    >
                      Dropdown
                    </button>
                    <ul
                      class="dropdown-menu"
                      aria-labelledby="btnGroupVerticalDrop1"
                    >
                      <li>
                        <a class="dropdown-item" href="#">Dropdown link</a>
                      </li>
                      <li>
                        <a class="dropdown-item" href="#">Dropdown link</a>
                      </li>
                    </ul>
                  </div>
                  <button type="button" class="btn btn-primary">Button</button>
                  <button type="button" class="btn btn-primary">Button</button>
                  <div class="btn-group" role="group">
                    <button
                      id="btnGroupVerticalDrop1"
                      type="button"
                      class="btn btn-primary dropdown-toggle"
                      data-bs-toggle="dropdown"
                      aria-expanded="false"
                    >
                      Dropdown
                    </button>
                    <ul
                      class="dropdown-menu"
                      aria-labelledby="btnGroupVerticalDrop1"
                    >
                      <li>
                        <a class="dropdown-item" href="#">Dropdown link</a>
                      </li>
                      <li>
                        <a class="dropdown-item" href="#">Dropdown link</a>
                      </li>
                    </ul>
                  </div>
                  <div class="btn-group" role="group">
                    <button
                      id="btnGroupVerticalDrop1"
                      type="button"
                      class="btn btn-primary dropdown-toggle"
                      data-bs-toggle="dropdown"
                      aria-expanded="false"
                    >
                      Dropdown
                    </button>
                    <ul
                      class="dropdown-menu"
                      aria-labelledby="btnGroupVerticalDrop1"
                    >
                      <li>
                        <a class="dropdown-item" href="#">Dropdown link</a>
                      </li>
                      <li>
                        <a class="dropdown-item" href="#">Dropdown link</a>
                      </li>
                    </ul>
                  </div>
                  <div class="btn-group" role="group">
                    <button
                      id="btnGroupVerticalDrop1"
                      type="button"
                      class="btn btn-primary dropdown-toggle"
                      data-bs-toggle="dropdown"
                      aria-expanded="false"
                    >
                      Dropdown
                    </button>
                    <ul
                      class="dropdown-menu"
                      aria-labelledby="btnGroupVerticalDrop1"
                    >
                      <li>
                        <a class="dropdown-item" href="#">Dropdown link</a>
                      </li>
                      <li>
                        <a class="dropdown-item" href="#">Dropdown link</a>
                      </li>
                    </ul>
                  </div>
                </div>
              </div>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Button Toolbar</h4>
            </template>
            <template v-slot:body>
              <p class="mb-4">
                Lorem Ipsum is simply dummy text of the printing and typesetting
                industry. Lorem Ipsum has been the industry's standard dummy
                text ever
              </p>
              <div
                class="btn-toolbar"
                role="toolbar"
                aria-label="Toolbar with button groups"
              >
                <b-button-group
                  class="btn-group-medium me-2"
                  role="group"
                  aria-label="First group"
                >
                  <b-button variant="primary">1</b-button>
                  <b-button variant="primary">2</b-button>
                  <b-button variant="primary">3</b-button>
                  <b-button variant="primary">4</b-button>
                </b-button-group>
                <b-button-group
                  class="btn-group-medium me-2"
                  role="group"
                  aria-label="Second group"
                >
                  <b-button variant="secondary">5</b-button>
                  <b-button variant="secondary">6</b-button>
                  <b-button variant="secondary">7</b-button>
                </b-button-group>
                <b-button-group
                  class="btn-group-medium"
                  role="group"
                  aria-label="Third group"
                >
                  <b-button variant="info">8</b-button>
                </b-button-group>
              </div>
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
  name: "UiButtons",
  mounted() {
    // socialvue.index()
  },
};
</script>
