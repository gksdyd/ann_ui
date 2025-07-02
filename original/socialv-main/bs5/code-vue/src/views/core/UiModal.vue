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
              <h3 class="text-white">Modal Page</h3>
              <p class="text-white">lorem ipsum</p>
            </div>
          </b-card>
        </b-col>
        <b-col sm="12" lg="6">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Modal components</h4>
            </template>

            <template v-slot:body>
              <p>
                Below is a <em>static</em> modal example (meaning its
                <code>position</code> and <code>display</code> have been
                overridden). Included are the modal header, modal body (required
                for <code>padding</code>), and modal footer (optional). We ask
                that you include modal headers with dismiss actions whenever
                possible, or provide another explicit dismiss action.
              </p>

              <button
                type="button"
                class="btn btn-primary"
                data-bs-toggle="modal"
                data-bs-target="#modal1"
              >
                Launch demo modal
              </button>
              <modal
                id="modal1"
                tabindex="-1"
                title="Create Post"
                aria-labelledby="modal1Label"
                aria-hidden="true"
              >
                <model-header>
                  <h5 class="modal-title" id="modal1Label">Modal Title</h5>
                  <button
                    :dismissable="true"
                    class="btn-close"
                    data-bs-dismiss="modal"
                    aria-label="Close"
                  ></button>
                </model-header>
                <model-body> </model-body>
                <model-footer>
                  <button
                    type="button"
                    class="btn btn-secondary"
                    data-bs-dismiss="modal"
                  >
                    Close
                  </button>
                  <button type="button" class="btn btn-primary">
                    Save changes
                  </button>
                </model-footer>
              </modal>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Modal Scrolling</h4>
            </template>

            <template v-slot:body>
              <p>
                When modals become too long for the user’s viewport or device,
                they scroll independent of the page itself. Try the demo below
                to see what we mean.
              </p>

              <button
                type="button"
                class="btn btn-primary"
                data-bs-toggle="modal"
                data-bs-target="#modal2"
              >
                Launch demo modal
              </button>
              <modal
                id="modal2"
                tabindex="-1"
                title="Create Post"
                aria-labelledby="modal2Label"
                aria-hidden="true"
                dialogClass="modal-dialog-scrollable"
              >
                <model-header>
                  <h5 class="modal-title" id="modal2Label">Modal Title</h5>
                  <button
                    :dismissable="true"
                    class="btn-close"
                    data-bs-dismiss="modal"
                    aria-label="Close"
                  ></button>
                </model-header>
                <model-body>
                  <p>
                    Cras mattis consectetur purus sit amet fermentum. Cras justo
                    odio, dapibus ac facilisis in, egestas eget quam. Morbi leo
                    risus, porta ac consectetur ac, vestibulum at eros.
                  </p>
                  <p>
                    Praesent commodo cursus magna, vel scelerisque nisl
                    consectetur et. Vivamus sagittis lacus vel augue laoreet
                    rutrum faucibus dolor auctor.
                  </p>
                  <p>
                    Aenean lacinia bibendum nulla sed consectetur. Praesent
                    commodo cursus magna, vel scelerisque nisl consectetur et.
                    Donec sed odio dui. Donec ullamcorper nulla non metus auctor
                    fringilla.
                  </p>
                  <p>
                    Cras mattis consectetur purus sit amet fermentum. Cras justo
                    odio, dapibus ac facilisis in, egestas eget quam. Morbi leo
                    risus, porta ac consectetur ac, vestibulum at eros.
                  </p>
                  <p>
                    Praesent commodo cursus magna, vel scelerisque nisl
                    consectetur et. Vivamus sagittis lacus vel augue laoreet
                    rutrum faucibus dolor auctor.
                  </p>
                  <p>
                    Aenean lacinia bibendum nulla sed consectetur. Praesent
                    commodo cursus magna, vel scelerisque nisl consectetur et.
                    Donec sed odio dui. Donec ullamcorper nulla non metus auctor
                    fringilla.
                  </p>
                  <p>
                    Cras mattis consectetur purus sit amet fermentum. Cras justo
                    odio, dapibus ac facilisis in, egestas eget quam. Morbi leo
                    risus, porta ac consectetur ac, vestibulum at eros.
                  </p>
                  <p>
                    Praesent commodo cursus magna, vel scelerisque nisl
                    consectetur et. Vivamus sagittis lacus vel augue laoreet
                    rutrum faucibus dolor auctor.
                  </p>
                  <p>
                    Aenean lacinia bibendum nulla sed consectetur. Praesent
                    commodo cursus magna, vel scelerisque nisl consectetur et.
                    Donec sed odio dui. Donec ullamcorper nulla non metus auctor
                    fringilla.
                  </p>
                  <p>
                    Cras mattis consectetur purus sit amet fermentum. Cras justo
                    odio, dapibus ac facilisis in, egestas eget quam. Morbi leo
                    risus, porta ac consectetur ac, vestibulum at eros.
                  </p>
                  <p>
                    Praesent commodo cursus magna, vel scelerisque nisl
                    consectetur et. Vivamus sagittis lacus vel augue laoreet
                    rutrum faucibus dolor auctor.
                  </p>
                  <p>
                    Aenean lacinia bibendum nulla sed consectetur. Praesent
                    commodo cursus magna, vel scelerisque nisl consectetur et.
                    Donec sed odio dui. Donec ullamcorper nulla non metus auctor
                    fringilla.
                  </p>
                  <p>
                    Cras mattis consectetur purus sit amet fermentum. Cras justo
                    odio, dapibus ac facilisis in, egestas eget quam. Morbi leo
                    risus, porta ac consectetur ac, vestibulum at eros.
                  </p>
                  <p>
                    Praesent commodo cursus magna, vel scelerisque nisl
                    consectetur et. Vivamus sagittis lacus vel augue laoreet
                    rutrum faucibus dolor auctor.
                  </p>
                  <p>
                    Aenean lacinia bibendum nulla sed consectetur. Praesent
                    commodo cursus magna, vel scelerisque nisl consectetur et.
                    Donec sed odio dui. Donec ullamcorper nulla non metus auctor
                    fringilla.
                  </p>
                  <p>
                    Cras mattis consectetur purus sit amet fermentum. Cras justo
                    odio, dapibus ac facilisis in, egestas eget quam. Morbi leo
                    risus, porta ac consectetur ac, vestibulum at eros.
                  </p>
                  <p>
                    Praesent commodo cursus magna, vel scelerisque nisl
                    consectetur et. Vivamus sagittis lacus vel augue laoreet
                    rutrum faucibus dolor auctor.
                  </p>
                  <p>
                    Aenean lacinia bibendum nulla sed consectetur. Praesent
                    commodo cursus magna, vel scelerisque nisl consectetur et.
                    Donec sed odio dui. Donec ullamcorper nulla non metus auctor
                    fringilla.
                  </p>
                </model-body>
                <model-footer>
                  <button
                    type="button"
                    class="btn btn-secondary"
                    data-bs-dismiss="modal"
                  >
                    Close
                  </button>
                  <button type="button" class="btn btn-primary">
                    Save changes
                  </button>
                </model-footer>
              </modal>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Optional sizes</h4>
            </template>

            <template v-slot:body>
              <p>
                Modals have three optional sizes, available via modifier classes
                to be placed on a .modal-dialog. These sizes kick in at certain
                breakpoints to avoid horizontal scrollbars on narrower
                viewports.
              </p>
              <button
                type="button"
                class="btn btn-primary mt-1"
                data-bs-toggle="modal"
                data-bs-target="#modal3"
              >
                Extra large modal
              </button>
              {{ "" }}
              <modal
                id="modal3"
                tabindex="-1"
                title="Create Post"
                aria-labelledby="modal3Label"
                aria-hidden="true"
                dialogClass="modal-xl"
              >
                <model-header>
                  <h5 class="modal-title" id="modal3Label">Modal Title</h5>
                  <button
                    :dismissable="true"
                    class="btn-close"
                    data-bs-dismiss="modal"
                    aria-label="Close"
                  ></button>
                </model-header>
                <model-body>
                  <p>Modal body text goes here.</p>
                </model-body>
                <model-footer>
                  <button
                    type="button"
                    class="btn btn-secondary"
                    data-bs-dismiss="modal"
                  >
                    Close
                  </button>
                  <button type="button" class="btn btn-primary">
                    Save changes
                  </button>
                </model-footer>
              </modal>
              <button
                type="button"
                class="btn btn-primary mt-1"
                data-bs-toggle="modal"
                data-bs-target="#modal4"
              >
                Large modal
              </button>
              {{ "" }}
              <modal
                id="modal4"
                tabindex="-1"
                title="Create Post"
                aria-labelledby="modal4Label"
                aria-hidden="true"
                dialogClass="modal-lg"
              >
                <model-header>
                  <h5 class="modal-title" id="modal4Label">Modal Title</h5>
                  <button
                    :dismissable="true"
                    class="btn-close"
                    data-bs-dismiss="modal"
                    aria-label="Close"
                  ></button>
                </model-header>
                <model-body>
                  <p>Modal body text goes here.</p>
                </model-body>
                <model-footer>
                  <button
                    type="button"
                    class="btn btn-secondary"
                    data-bs-dismiss="modal"
                  >
                    Close
                  </button>
                  <button type="button" class="btn btn-primary">
                    Save changes
                  </button>
                </model-footer>
              </modal>
              <button
                type="button"
                class="btn btn-primary mt-1"
                data-bs-toggle="modal"
                data-bs-target="#modal5"
              >
                Small modal
              </button>
              <modal
                id="modal5"
                tabindex="-1"
                title="Create Post"
                aria-labelledby="modal4Label"
                aria-hidden="true"
                dialogClass="modal-sm"
              >
                <model-header>
                  <h5 class="modal-title" id="modal5Label">Modal Title</h5>
                  <button
                    :dismissable="true"
                    class="btn-close"
                    data-bs-dismiss="modal"
                    aria-label="Close"
                  ></button>
                </model-header>
                <model-body>
                  <p>Modal body text goes here.</p>
                </model-body>
                <model-footer>
                  <button
                    type="button"
                    class="btn btn-secondary"
                    data-bs-dismiss="modal"
                  >
                    Close
                  </button>
                  <button type="button" class="btn btn-primary">
                    Save changes
                  </button>
                </model-footer>
              </modal>
            </template>
          </iq-card>
        </b-col>
        <b-col lg="6" sm="12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Scrolling long content</h4>
            </template>

            <template v-slot:body>
              <p>
                When modals become too long for the user’s viewport or device,
                they scroll independent of the page itself. Try the demo below
                to see what we mean.
              </p>

              <button
                type="button"
                class="btn btn-primary"
                data-bs-toggle="modal"
                data-bs-target="#modal6"
              >
                Launch demo modal
              </button>
              <modal
                id="modal6"
                tabindex="-1"
                title="Create Post"
                aria-labelledby="modal6Label"
                aria-hidden="true"
              >
                <model-header>
                  <h5 class="modal-title" id="modal6Label">Modal Title</h5>
                  <button
                    :dismissable="true"
                    class="btn-close"
                    data-bs-dismiss="modal"
                    aria-label="Close"
                  ></button>
                </model-header>
                <model-body>
                  <p>
                    Cras mattis consectetur purus sit amet fermentum. Cras justo
                    odio, dapibus ac facilisis in, egestas eget quam. Morbi leo
                    risus, porta ac consectetur ac, vestibulum at eros.
                  </p>
                  <p>
                    Praesent commodo cursus magna, vel scelerisque nisl
                    consectetur et. Vivamus sagittis lacus vel augue laoreet
                    rutrum faucibus dolor auctor.
                  </p>
                  <p>
                    Aenean lacinia bibendum nulla sed consectetur. Praesent
                    commodo cursus magna, vel scelerisque nisl consectetur et.
                    Donec sed odio dui. Donec ullamcorper nulla non metus auctor
                    fringilla.
                  </p>
                  <p>
                    Cras mattis consectetur purus sit amet fermentum. Cras justo
                    odio, dapibus ac facilisis in, egestas eget quam. Morbi leo
                    risus, porta ac consectetur ac, vestibulum at eros.
                  </p>
                  <p>
                    Praesent commodo cursus magna, vel scelerisque nisl
                    consectetur et. Vivamus sagittis lacus vel augue laoreet
                    rutrum faucibus dolor auctor.
                  </p>
                  <p>
                    Aenean lacinia bibendum nulla sed consectetur. Praesent
                    commodo cursus magna, vel scelerisque nisl consectetur et.
                    Donec sed odio dui. Donec ullamcorper nulla non metus auctor
                    fringilla.
                  </p>
                  <p>
                    Cras mattis consectetur purus sit amet fermentum. Cras justo
                    odio, dapibus ac facilisis in, egestas eget quam. Morbi leo
                    risus, porta ac consectetur ac, vestibulum at eros.
                  </p>
                  <p>
                    Praesent commodo cursus magna, vel scelerisque nisl
                    consectetur et. Vivamus sagittis lacus vel augue laoreet
                    rutrum faucibus dolor auctor.
                  </p>
                  <p>
                    Aenean lacinia bibendum nulla sed consectetur. Praesent
                    commodo cursus magna, vel scelerisque nisl consectetur et.
                    Donec sed odio dui. Donec ullamcorper nulla non metus auctor
                    fringilla.
                  </p>
                  <p>
                    Cras mattis consectetur purus sit amet fermentum. Cras justo
                    odio, dapibus ac facilisis in, egestas eget quam. Morbi leo
                    risus, porta ac consectetur ac, vestibulum at eros.
                  </p>
                  <p>
                    Praesent commodo cursus magna, vel scelerisque nisl
                    consectetur et. Vivamus sagittis lacus vel augue laoreet
                    rutrum faucibus dolor auctor.
                  </p>
                  <p>
                    Aenean lacinia bibendum nulla sed consectetur. Praesent
                    commodo cursus magna, vel scelerisque nisl consectetur et.
                    Donec sed odio dui. Donec ullamcorper nulla non metus auctor
                    fringilla.
                  </p>
                  <p>
                    Cras mattis consectetur purus sit amet fermentum. Cras justo
                    odio, dapibus ac facilisis in, egestas eget quam. Morbi leo
                    risus, porta ac consectetur ac, vestibulum at eros.
                  </p>
                  <p>
                    Praesent commodo cursus magna, vel scelerisque nisl
                    consectetur et. Vivamus sagittis lacus vel augue laoreet
                    rutrum faucibus dolor auctor.
                  </p>
                  <p>
                    Aenean lacinia bibendum nulla sed consectetur. Praesent
                    commodo cursus magna, vel scelerisque nisl consectetur et.
                    Donec sed odio dui. Donec ullamcorper nulla non metus auctor
                    fringilla.
                  </p>
                  <p>
                    Cras mattis consectetur purus sit amet fermentum. Cras justo
                    odio, dapibus ac facilisis in, egestas eget quam. Morbi leo
                    risus, porta ac consectetur ac, vestibulum at eros.
                  </p>
                  <p>
                    Praesent commodo cursus magna, vel scelerisque nisl
                    consectetur et. Vivamus sagittis lacus vel augue laoreet
                    rutrum faucibus dolor auctor.
                  </p>
                  <p>
                    Aenean lacinia bibendum nulla sed consectetur. Praesent
                    commodo cursus magna, vel scelerisque nisl consectetur et.
                    Donec sed odio dui. Donec ullamcorper nulla non metus auctor
                    fringilla.
                  </p>
                </model-body>
                <model-footer>
                  <button
                    type="button"
                    class="btn btn-secondary"
                    data-bs-dismiss="modal"
                  >
                    Close
                  </button>
                  <button type="button" class="btn btn-primary">
                    Save changes
                  </button>
                </model-footer>
              </modal>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Vertically centered</h4>
            </template>

            <template v-slot:body>
              <p>
                Add
                <code class="highlighter-rouge">.modal-dialog-centered</code> to
                <code class="highlighter-rouge">.modal-dialog</code> to
                vertically center the modal.
              </p>

              <button
                type="button"
                class="btn btn-primary mb-1"
                data-bs-toggle="modal"
                data-bs-target="#modal7"
              >
                Launch demo modal
              </button>
              {{ "" }}
              <modal
                id="modal7"
                tabindex="-1"
                title="Create Post"
                aria-labelledby="modal7Label"
                aria-hidden="true"
                dialogClass="modal-dialog-centered"
              >
                <model-header>
                  <h5 class="modal-title" id="modal7Label">Modal Title</h5>
                  <button
                    :dismissable="true"
                    class="btn-close"
                    data-bs-dismiss="modal"
                    aria-label="Close"
                  ></button>
                </model-header>
                <model-body>
                  <p>Modal body text goes here.</p>
                </model-body>
                <model-footer>
                  <button
                    type="button"
                    class="btn btn-secondary"
                    data-bs-dismiss="modal"
                  >
                    Close
                  </button>
                  <button type="button" class="btn btn-primary">
                    Save changes
                  </button>
                </model-footer>
              </modal>
              <button
                type="button"
                class="btn btn-primary me-1 mb-1"
                data-bs-toggle="modal"
                data-bs-target="#modal8"
              >
                Vertically centered scrollable modal
              </button>
              <modal
                id="modal8"
                tabindex="-1"
                title="Create Post"
                aria-labelledby="modal8Label"
                aria-hidden="true"
                dialogClass="modal-dialog-centered modal-dialog-scrollable"
              >
                <model-header>
                  <h5 class="modal-title" id="modal8Label">Modal Title</h5>
                  <button
                    :dismissable="true"
                    class="btn-close"
                    data-bs-dismiss="modal"
                    aria-label="Close"
                  ></button>
                </model-header>
                <model-body>
                  <p>
                    Cras mattis consectetur purus sit amet fermentum. Cras justo
                    odio, dapibus ac facilisis in, egestas eget quam. Morbi leo
                    risus, porta ac consectetur ac, vestibulum at eros.
                  </p>
                  <p>
                    Praesent commodo cursus magna, vel scelerisque nisl
                    consectetur et. Vivamus sagittis lacus vel augue laoreet
                    rutrum faucibus dolor auctor.
                  </p>
                  <p>
                    Aenean lacinia bibendum nulla sed consectetur. Praesent
                    commodo cursus magna, vel scelerisque nisl consectetur et.
                    Donec sed odio dui. Donec ullamcorper nulla non metus auctor
                    fringilla.
                  </p>
                  <p>
                    Cras mattis consectetur purus sit amet fermentum. Cras justo
                    odio, dapibus ac facilisis in, egestas eget quam. Morbi leo
                    risus, porta ac consectetur ac, vestibulum at eros.
                  </p>
                  <p>
                    Praesent commodo cursus magna, vel scelerisque nisl
                    consectetur et. Vivamus sagittis lacus vel augue laoreet
                    rutrum faucibus dolor auctor.
                  </p>
                  <p>
                    Aenean lacinia bibendum nulla sed consectetur. Praesent
                    commodo cursus magna, vel scelerisque nisl consectetur et.
                    Donec sed odio dui. Donec ullamcorper nulla non metus auctor
                    fringilla.
                  </p>
                  <p>
                    Cras mattis consectetur purus sit amet fermentum. Cras justo
                    odio, dapibus ac facilisis in, egestas eget quam. Morbi leo
                    risus, porta ac consectetur ac, vestibulum at eros.
                  </p>
                  <p>
                    Praesent commodo cursus magna, vel scelerisque nisl
                    consectetur et. Vivamus sagittis lacus vel augue laoreet
                    rutrum faucibus dolor auctor.
                  </p>
                  <p>
                    Aenean lacinia bibendum nulla sed consectetur. Praesent
                    commodo cursus magna, vel scelerisque nisl consectetur et.
                    Donec sed odio dui. Donec ullamcorper nulla non metus auctor
                    fringilla.
                  </p>
                  <p>
                    Cras mattis consectetur purus sit amet fermentum. Cras justo
                    odio, dapibus ac facilisis in, egestas eget quam. Morbi leo
                    risus, porta ac consectetur ac, vestibulum at eros.
                  </p>
                  <p>
                    Praesent commodo cursus magna, vel scelerisque nisl
                    consectetur et. Vivamus sagittis lacus vel augue laoreet
                    rutrum faucibus dolor auctor.
                  </p>
                  <p>
                    Aenean lacinia bibendum nulla sed consectetur. Praesent
                    commodo cursus magna, vel scelerisque nisl consectetur et.
                    Donec sed odio dui. Donec ullamcorper nulla non metus auctor
                    fringilla.
                  </p>
                  <p>
                    Cras mattis consectetur purus sit amet fermentum. Cras justo
                    odio, dapibus ac facilisis in, egestas eget quam. Morbi leo
                    risus, porta ac consectetur ac, vestibulum at eros.
                  </p>
                  <p>
                    Praesent commodo cursus magna, vel scelerisque nisl
                    consectetur et. Vivamus sagittis lacus vel augue laoreet
                    rutrum faucibus dolor auctor.
                  </p>
                  <p>
                    Aenean lacinia bibendum nulla sed consectetur. Praesent
                    commodo cursus magna, vel scelerisque nisl consectetur et.
                    Donec sed odio dui. Donec ullamcorper nulla non metus auctor
                    fringilla.
                  </p>
                  <p>
                    Cras mattis consectetur purus sit amet fermentum. Cras justo
                    odio, dapibus ac facilisis in, egestas eget quam. Morbi leo
                    risus, porta ac consectetur ac, vestibulum at eros.
                  </p>
                  <p>
                    Praesent commodo cursus magna, vel scelerisque nisl
                    consectetur et. Vivamus sagittis lacus vel augue laoreet
                    rutrum faucibus dolor auctor.
                  </p>
                  <p>
                    Aenean lacinia bibendum nulla sed consectetur. Praesent
                    commodo cursus magna, vel scelerisque nisl consectetur et.
                    Donec sed odio dui. Donec ullamcorper nulla non metus auctor
                    fringilla.
                  </p>
                </model-body>
                <model-footer>
                  <button
                    type="button"
                    class="btn btn-secondary"
                    data-bs-dismiss="modal"
                  >
                    Close
                  </button>
                  <button type="button" class="btn btn-primary">
                    Save changes
                  </button>
                </model-footer>
              </modal>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Using the grid</h4>
            </template>

            <template v-slot:body>
              <p>
                Utilize the Bootstrap grid system within a modal by nesting
                <code>.container-fluid</code> within the
                <code>.modal-body</code>. Then, use the normal grid system
                classes as you would anywhere else.
              </p>
              <button
                type="button"
                class="btn btn-primary"
                data-bs-toggle="modal"
                data-bs-target="#modal9"
              >
                Launch demo modal
              </button>
              <modal
                id="modal9"
                tabindex="-1"
                title="Create Post"
                aria-labelledby="modal9Label"
                aria-hidden="true"
              >
                <model-header>
                  <h5 class="modal-title" id="modal9Label">Modal Title</h5>
                  <button
                    :dismissable="true"
                    class="btn-close"
                    data-bs-dismiss="modal"
                    aria-label="Close"
                  ></button>
                </model-header>
                <model-body>
                  <div class="iq-example-row">
                    <b-container fluid>
                      <b-row class="mb-3">
                        <b-col md="4">.col-md-4</b-col>
                        <b-col md="4" ms="auto">.col-md-4 .ms-auto</b-col>
                      </b-row>
                      <b-row class="mb-3">
                        <b-col md="3" ms="auto">.col-md-3 .ms-auto</b-col>
                        <b-col md="2" ms="auto">.col-md-2 .ms-auto</b-col>
                      </b-row>
                      <b-row class="mb-3">
                        <b-col md="6" ms="auto">.col-md-6 .ms-auto</b-col>
                      </b-row>
                      <b-row>
                        <b-col sm="9">
                          Level 1: .col-sm-9
                          <b-row>
                            <b-col cols="8" sm="6">
                              Level 2: .col-8 .col-sm-6
                            </b-col>
                            <b-col cols="4" sm="6">
                              Level 2: .col-4 .col-sm-6
                            </b-col>
                          </b-row>
                        </b-col>
                      </b-row>
                    </b-container>
                  </div>
                </model-body>
                <model-footer>
                  <button
                    type="button"
                    class="btn btn-secondary"
                    data-bs-dismiss="modal"
                  >
                    Close
                  </button>
                  <button type="button" class="btn btn-primary">
                    Save changes
                  </button>
                </model-footer>
              </modal>
            </template>
          </iq-card>
        </b-col>
        <b-col sm="12" lg="12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Fullscreen Modal</h4>
            </template>
            <template v-slot:body>
              <p>
                Another override is the option to pop up a modal that covers the
                user viewport, available via modifier classes that are placed on
                a <code>.modal-dialog</code>.
              </p>
              <div class="bd-example">
                <button
                  type="button"
                  class="btn btn-primary"
                  data-bs-toggle="modal"
                  data-bs-target="#exampleModalFullscreen"
                >
                  Full screen
                </button>
                {{ "" }}
                <button
                  type="button"
                  class="btn btn-primary"
                  data-bs-toggle="modal"
                  data-bs-target="#exampleModalFullscreenSm"
                >
                  Full screen below sm
                </button>
                {{ "" }}
                <button
                  type="button"
                  class="btn btn-primary"
                  data-bs-toggle="modal"
                  data-bs-target="#exampleModalFullscreenMd"
                >
                  Full screen below md
                </button>
                {{ "" }}
                <button
                  type="button"
                  class="btn btn-primary"
                  data-bs-toggle="modal"
                  data-bs-target="#exampleModalFullscreenLg"
                >
                  Full screen below lg
                </button>
                {{ "" }}
                <button
                  type="button"
                  class="btn btn-primary"
                  data-bs-toggle="modal"
                  data-bs-target="#exampleModalFullscreenXl"
                >
                  Full screen below xl
                </button>
                {{ "" }}
                <button
                  type="button"
                  class="btn btn-primary"
                  data-bs-toggle="modal"
                  data-bs-target="#exampleModalFullscreenXxl"
                >
                  Full screen below xxl
                </button>
              </div>
              <modal
                id="exampleModalFullscreen"
                tabindex="-1"
                title="Create Post"
                aria-labelledby="exampleModalFullscreenLabel"
                aria-hidden="true"
                dialogClass="modal-fullscreen"
              >
                <model-header>
                  <h5 class="modal-title" id="exampleModalFullscreenLabel">
                    Full screen modal
                  </h5>
                  <button
                    :dismissable="true"
                    class="btn-close"
                    data-bs-dismiss="modal"
                    aria-label="Close"
                  ></button>
                </model-header>
                <model-body> </model-body>
                <model-footer>
                  <button
                    type="button"
                    class="btn btn-secondary"
                    data-bs-dismiss="modal"
                  >
                    Close
                  </button>
                </model-footer>
              </modal>
              <modal
                id="exampleModalFullscreenSm"
                tabindex="-1"
                title="Create Post"
                aria-labelledby="exampleModalFullscreenSmLabel"
                aria-hidden="true"
                dialogClass="modal-fullscreen-sm-down"
              >
                <model-header>
                  <h5 class="modal-title" id="exampleModalFullscreenSmLabel">
                    Full screen below sm
                  </h5>
                  <button
                    :dismissable="true"
                    class="btn-close"
                    data-bs-dismiss="modal"
                    aria-label="Close"
                  ></button>
                </model-header>
                <model-body> </model-body>
                <model-footer>
                  <button
                    type="button"
                    class="btn btn-secondary"
                    data-bs-dismiss="modal"
                  >
                    Close
                  </button>
                </model-footer>
              </modal>
              <modal
                id="exampleModalFullscreenMd"
                tabindex="-1"
                title="Create Post"
                aria-labelledby="exampleModalFullscreenMdLabel"
                aria-hidden="true"
                dialogClass="modal-fullscreen-md-down"
              >
                <model-header>
                  <h5 class="modal-title" id="exampleModalFullscreenMdLabel">
                    Full screen below md
                  </h5>
                  <button
                    :dismissable="true"
                    class="btn-close"
                    data-bs-dismiss="modal"
                    aria-label="Close"
                  ></button>
                </model-header>
                <model-body> </model-body>
                <model-footer>
                  <button
                    type="button"
                    class="btn btn-secondary"
                    data-bs-dismiss="modal"
                  >
                    Close
                  </button>
                </model-footer>
              </modal>
              <modal
                id="exampleModalFullscreenLg"
                tabindex="-1"
                title="Create Post"
                aria-labelledby="exampleModalFullscreenLgLabel"
                aria-hidden="true"
                dialogClass="modal-fullscreen-lg-down"
              >
                <model-header>
                  <h5 class="modal-title" id="exampleModalFullscreenLgLabel">
                    Full screen below lg
                  </h5>
                  <button
                    :dismissable="true"
                    class="btn-close"
                    data-bs-dismiss="modal"
                    aria-label="Close"
                  ></button>
                </model-header>
                <model-body> </model-body>
                <model-footer>
                  <button
                    type="button"
                    class="btn btn-secondary"
                    data-bs-dismiss="modal"
                  >
                    Close
                  </button>
                </model-footer>
              </modal>
              <modal
                id="exampleModalFullscreenXl"
                tabindex="-1"
                title="Create Post"
                aria-labelledby="exampleModalFullscreenXlLabel"
                aria-hidden="true"
                dialogClass="modal-fullscreen-xl-down"
              >
                <model-header>
                  <h5 class="modal-title" id="exampleModalFullscreenXlLabel">
                    Full screen below xl
                  </h5>
                  <button
                    :dismissable="true"
                    class="btn-close"
                    data-bs-dismiss="modal"
                    aria-label="Close"
                  ></button>
                </model-header>
                <model-body> </model-body>
                <model-footer>
                  <button
                    type="button"
                    class="btn btn-secondary"
                    data-bs-dismiss="modal"
                  >
                    Close
                  </button>
                </model-footer>
              </modal>
              <modal
                id="exampleModalFullscreenXxl"
                tabindex="-1"
                title="Create Post"
                aria-labelledby="exampleModalFullscreenXxlLabel"
                aria-hidden="true"
                dialogClass="modal-fullscreen-xxl-down"
              >
                <model-header>
                  <h5 class="modal-title" id="exampleModalFullscreenXxlLabel">
                    Full screen below Xxl
                  </h5>
                  <button
                    :dismissable="true"
                    class="btn-close"
                    data-bs-dismiss="modal"
                    aria-label="Close"
                  ></button>
                </model-header>
                <model-body> </model-body>
                <model-footer>
                  <button
                    type="button"
                    class="btn btn-secondary"
                    data-bs-dismiss="modal"
                  >
                    Close
                  </button>
                </model-footer>
              </modal>
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
  name: "UiModal",
  mounted() {
    // socialvue.index()
  },
};
</script>
