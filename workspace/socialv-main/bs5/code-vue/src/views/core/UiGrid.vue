<template>
  <div class="content-inner">
    <b-container>
      <b-row>
        <b-col sm="12">
          <div
            class="card position-relative inner-page-bg bg-primary"
            style="height: 150px"
          >
            <div class="inner-page-title">
              <h3 class="text-white">Grid Page</h3>
              <p class="text-white">lorem ipsum</p>
            </div>
          </div>
        </b-col>
        <b-col sm="12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Grid options</h4>
            </template>
            <template v-slot:body>
              <p>
                See how aspects of the Bootstrap grid system work across
                multiple devices with a handy table..
              </p>
              <div class="table-responsive">
                <table class="table table-bordered table-striped mb-0">
                  <thead>
                    <tr>
                      <th></th>
                      <th class="text-center">
                        Extra small <br />
                        <small>&lt;576px</small>
                      </th>
                      <th class="text-center">
                        Small<br />
                        <small> ≥576px</small>
                      </th>
                      <th class="text-center">
                        Medium<br />
                        <small>≥768px</small>
                      </th>
                      <th class="text-center">
                        Large<br />
                        <small>≥992px</small>
                      </th>
                      <th class="text-center">
                        Extra large<br />
                        <small>≥1200px</small>
                      </th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <th class="text-nowrap text-left" scope="row">
                        Max container width
                      </th>
                      <td>None (auto)</td>
                      <td>540px</td>
                      <td>720px</td>
                      <td>960px</td>
                      <td>1140px</td>
                    </tr>
                    <tr>
                      <th class="text-nowrap text-left" scope="row">
                        Class prefix
                      </th>
                      <td><code>.col-</code></td>
                      <td><code>.col-sm-</code></td>
                      <td><code>.col-md-</code></td>
                      <td><code>.col-lg-</code></td>
                      <td><code>.col-xl-</code></td>
                    </tr>
                    <tr>
                      <th class="text-nowrap text-left" scope="row">
                        # of columns
                      </th>
                      <td colspan="5">12</td>
                    </tr>
                    <tr>
                      <th class="text-nowrap text-left" scope="row">
                        Gutter width
                      </th>
                      <td colspan="5">30px (15px on each side of a column)</td>
                    </tr>
                    <tr>
                      <th class="text-nowrap text-left" scope="row">
                        Nestable
                      </th>
                      <td colspan="5">Yes</td>
                    </tr>
                    <!-- <tr>
                    <th class="text-nowrap text-left" scope="row">Offset</th>
                    <td><code>offset="*"</code></td>
                    <td><code>offset-sm="*"</code></td>
                    <td><code>offset-md="*"</code></td>
                    <td><code>offset-lg="*"</code></td>
                    <td><code>offset-xl="*"</code></td>
                  </tr> -->
                    <tr>
                      <th class="text-nowrap text-left" scope="row">
                        Column ordering
                      </th>
                      <td colspan="5">Yes</td>
                    </tr>
                  </tbody>
                </table>
              </div>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Equal-width</h4>
            </template>

            <template v-slot:body>
              <p>
                For example, here are two grid layouts that apply to every
                device and viewport, from <code>xs</code> to <code>xl</code>.
                Add any number of unit-less classes for each breakpoint you need
                and every column will be the same width.
              </p>

              <div class="iq-example-row">
                <b-container fluid>
                  <!-- Stack the columns on mobile by making one full-width and the other half-width -->
                  <b-row class="mb-3">
                    <b-col md="8" cols="12">.col-12 .col-md-8</b-col>
                    <b-col md="4" cols="6">.col-6 .col-md-4</b-col>
                  </b-row>
                  <!-- Columns start at 50% wide on mobile and bump up to 33.3% wide on desktop -->
                  <b-row class="mb-3">
                    <b-col cols="6" md="4">.col-6 .col-md-4</b-col>
                    <b-col cols="6" md="4">.col-6 .col-md-4</b-col>
                    <b-col cols="6" md="4">.col-6 .col-md-4</b-col>
                  </b-row>
                  <!-- Columns are always 50% wide, on mobile and desktop -->
                  <b-row>
                    <div class="col-6">.col-6</div>
                    <div class="col-6">.col-6</div>
                  </b-row>
                </b-container>
              </div>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Setting one column width</h4>
            </template>

            <template v-slot:body>
              <p>
                Auto-layout for flexbox grid columns also means you can set the
                width of one column and have the sibling columns automatically
                resize around it. You may use predefined grid classes (as shown
                below), grid mixins, or inline widths. Note that the other
                columns will resize no matter the width of the center column.
              </p>

              <div class="iq-example-row">
                <b-container fluid>
                  <b-row class="mb-3">
                    <b-col>1 of 3</b-col>
                    <b-col cols="6">2 of 3 (wider)</b-col>
                    <b-col>3 of 3</b-col>
                  </b-row>
                  <b-row>
                    <b-col>1 of 3</b-col>
                    <b-col cols="5" class="col-5">2 of 3 (wider)</b-col>
                    <b-col>3 of 3</b-col>
                  </b-row>
                </b-container>
              </div>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Variable width content</h4>
            </template>

            <template v-slot:body>
              <p>
                Use <code>col-{breakpoint}-auto</code> classes to size columns
                based on the natural width of their content.
              </p>

              <div class="iq-example-row">
                <b-container fluid>
                  <b-row class="justify-content-md-center mb-3">
                    <b-col lg="2">1 of 3</b-col>
                    <b-col md="auto">Variable width content</b-col>
                    <b-col lg="2">3 of 3</b-col>
                  </b-row>
                  <b-row>
                    <b-col>1 of 3</b-col>
                    <b-col md="auto">Variable width content</b-col>
                    <b-col lg="2">3 of 3</b-col>
                  </b-row>
                </b-container>
              </div>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Equal-width multi-row</h4>
            </template>

            <template v-slot:body>
              <p>
                Create equal-width columns that span multiple rows by inserting
                a <code>.w-100</code> where you want the columns to break to a
                new line. Make the breaks responsive by mixing the
                <code>.w-100</code> with some
                <a href="/docs/4.3/utilities/display/"
                  >responsive display utilities</a
                >.
              </p>

              <div class="iq-example-row">
                <b-container fluid>
                  <b-row>
                    <b-col>col</b-col>
                    <b-col>col</b-col>
                    <div class="w-100"></div>
                    <b-col>col</b-col>
                    <b-col>col</b-col>
                  </b-row>
                </b-container>
              </div>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Responsive classes</h4>
            </template>

            <template v-slot:body>
              <p>
                Bootstrap’s grid includes five tiers of predefined classes for
                building complex responsive layouts. Customize the size of your
                columns on extra small, small, medium, large, or extra large
                devices however you see fit.
              </p>
              <h4 class="card-title">All breakpoints</h4>
              <p>
                For grids that are the same from the smallest of devices to the
                largest, use the <code>.col</code> and
                <code>.col-*</code> classes. Specify a numbered class when you
                need a particularly sized column; otherwise, feel free to stick
                to <code>.col</code>.
              </p>

              <div class="iq-example-row">
                <b-container fluid>
                  <b-row class="mb-3">
                    <b-col>col</b-col>
                    <b-col>col</b-col>
                    <b-col>col</b-col>
                    <b-col>col</b-col>
                  </b-row>
                  <b-row>
                    <b-col cols="8">col-8</b-col>
                    <b-col cols="4">col-4</b-col>
                  </b-row>
                </b-container>
              </div>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Stacked to horizontal</h4>
            </template>

            <template v-slot:body>
              <p>
                Using a single set of <code>.col-sm-*</code> classes, you can
                create a basic grid system that starts out stacked and becomes
                horizontal at the small breakpoint (<code>sm</code>).
              </p>

              <div class="iq-example-row">
                <b-container fluid>
                  <b-row class="mb-3">
                    <b-col sm="8">col-sm-8</b-col>
                    <b-col sm="4">col-sm-4</b-col>
                  </b-row>
                  <b-row>
                    <div class="col-sm">col-sm</div>
                    <div class="col-sm">col-sm</div>
                    <div class="col-sm">col-sm</div>
                  </b-row>
                </b-container>
              </div>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Mix and match</h4>
            </template>

            <template v-slot:body>
              <p>
                Don’t want your columns to simply stack in some grid tiers? Use
                a combination of different classes for each tier as needed. See
                the example below for a better idea of how it all works.
              </p>

              <div class="iq-example-row">
                <b-container fluid>
                  <!-- Stack the columns on mobile by making one full-width and the other half-width -->
                  <b-row class="mb-3">
                    <div class="col-12 col-md-8">.col-12 .col-md-8</div>
                    <b-col cols="6" md="4">.col-6 .col-md-4</b-col>
                  </b-row>
                  <!-- Columns start at 50% wide on mobile and bump up to 33.3% wide on desktop -->
                  <b-row class="mb-3">
                    <b-col cols="6" md="4">.col-6 .col-md-4</b-col>
                    <b-col cols="6" md="4">.col-6 .col-md-4</b-col>
                    <b-col cols="6" md="4">.col-6 .col-md-4</b-col>
                  </b-row>
                  <!-- Columns are always 50% wide, on mobile and desktop -->
                  <b-row>
                    <div class="col-6">.col-6</div>
                    <div class="col-6">.col-6</div>
                  </b-row>
                </b-container>
              </div>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Gutters</h4>
            </template>

            <template v-slot:body>
              <p>
                Gutters can be responsively adjusted by breakpoint-specific
                padding and negative margin utility classes. To change the
                gutters in a given row, pair a negative margin utility on the
                <code>.row</code> and matching padding utilities on the
                <code>.col</code>s. The <code>.container</code> or
                <code>.container-fluid</code> parent may need to be adjusted too
                to avoid unwanted overflow, using again matching padding
                utility.
              </p>
              <p>
                Here’s an example of customizing the Bootstrap grid at the large
                (<code>lg</code>) breakpoint and above. We’ve increased the
                <code>.col</code> padding with <code>.px-lg-5</code>,
                counteracted that with <code>.mx-lg-n5</code> on the parent
                <code>.row</code> and then adjusted the
                <code>.container</code> wrapper with <code>.px-lg-5</code>.
              </p>

              <div class="iq-example-row">
                <b-container fluid class="container-fluid px-lg-5">
                  <b-row class="mx-lg-n5">
                    <b-col class="py-3 px-lg-5 border bg-light">
                      Custom column padding
                    </b-col>
                    <b-col class="py-3 px-lg-5 border bg-light">
                      Custom column padding
                    </b-col>
                  </b-row>
                </b-container>
              </div>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Alignment</h4>
            </template>

            <template v-slot:body>
              <p>
                Use flexbox alignment utilities to vertically and horizontally
                align columns.
                <strong
                  >Internet Explorer 10-11 do not support vertical alignment of
                  flex items when the flex container has a
                  <code>min-height</code> as shown below.</strong
                >
                {{ "" }}
                <a href="https://github.com/philipwalton/flexbugs#flexbug-3"
                  >See Flexbugs #3 for more details.</a
                >
              </p>
              <h4 class="mb-3">Vertical alignment</h4>

              <div class="iq-example-row iq-example-row-flex-cols">
                <b-container fluid>
                  <b-row class="align-items-start">
                    <b-col>One of three columns</b-col>
                    <b-col>One of three columns</b-col>
                    <b-col>One of three columns</b-col>
                  </b-row>
                  <b-row class="align-items-center">
                    <b-col>One of three columns</b-col>
                    <b-col>One of three columns</b-col>
                    <b-col>One of three columns</b-col>
                  </b-row>
                  <b-row class="align-items-end">
                    <b-col>One of three columns</b-col>
                    <b-col>One of three columns</b-col>
                    <b-col>One of three columns</b-col>
                  </b-row>
                </b-container>
                <b-container fluid>
                  <b-row>
                    <b-col class="align-self-start">One of three columns</b-col>
                    <b-col class="align-self-center">
                      One of three columns
                    </b-col>
                    <b-col class="align-self-end">One of three columns</b-col>
                  </b-row>
                </b-container>
              </div>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Horizontal alignment</h4>
            </template>

            <template v-slot:body>
              <p>
                Create equal-width columns that span multiple rows by inserting
                a <code>.w-100</code> where you want the columns to break to a
                new line. Make the breaks responsive by mixing the
                <code>.w-100</code> with some
                <a href="/docs/4.3/utilities/display/"
                  >responsive display utilities</a
                >.
              </p>

              <div class="iq-example-row">
                <b-container fluid>
                  <b-row class="justify-content-start mb-3">
                    <div class="col-4">One of two columns</div>
                    <div class="col-4">One of two columns</div>
                  </b-row>
                  <b-row class="justify-content-center mb-3">
                    <div class="col-4">One of two columns</div>
                    <div class="col-4">One of two columns</div>
                  </b-row>
                  <b-row class="justify-content-end mb-3">
                    <div class="col-4">One of two columns</div>
                    <div class="col-4">One of two columns</div>
                  </b-row>
                  <b-row class="justify-content-around mb-3">
                    <div class="col-4">One of two columns</div>
                    <div class="col-4">One of two columns</div>
                  </b-row>
                  <b-row class="justify-content-between">
                    <div class="col-4">One of two columns</div>
                    <div class="col-4">One of two columns</div>
                  </b-row>
                </b-container>
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
  name: "UiGrid",
  mounted() {
    // socialvue.index()
  },
};
</script>
