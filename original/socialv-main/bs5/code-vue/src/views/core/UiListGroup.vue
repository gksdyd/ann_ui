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
              <h3 class="text-white">List Group Page</h3>
              <p class="text-white">lorem ipsum</p>
            </div>
          </div>
        </b-col>
        <b-col lg="6" sm="12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">List group</h4>
            </template>

            <template v-slot:body>
              <p>
                The most basic list group is an unordered list with list items
                and the proper classes. Build upon it with the options that
                follow, or with your own CSS as needed.
              </p>
              <ul class="list-group">
                <li class="list-group-item">Cras justo odio</li>
                <li class="list-group-item">Dapibus ac facilisis in</li>
                <li class="list-group-item">Morbi leo risus</li>
                <li class="list-group-item">Porta ac consectetur ac</li>
                <li class="list-group-item">Vestibulum at eros</li>
              </ul>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Disabled items</h4>
            </template>

            <template v-slot:body>
              <p>
                Add <code>.disabled</code> to a <code>.list-group-item</code> to
                make it <em>appear</em> disabled. Note that some elements with
                <code>.disabled</code> will also require custom JavaScript to
                fully disable their click events (e.g., links).
              </p>
              <ul class="list-group">
                <li class="list-group-item disabled" aria-disabled="true">
                  Cras justo odio
                </li>
                <li class="list-group-item">Dapibus ac facilisis in</li>
                <li class="list-group-item">Morbi leo risus</li>
                <li class="list-group-item">Porta ac consectetur ac</li>
                <li class="list-group-item">Vestibulum at eros</li>
              </ul>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Flush</h4>
            </template>

            <template v-slot:body>
              <p>
                Add <code class="highlighter-rouge">.list-group-flush</code> to
                remove some borders and rounded corners to render list group
                items edge-to-edge in a parent container (e.g., cards).
              </p>
              <ul class="list-group list-group-flush">
                <li class="list-group-item">Cras justo odio</li>
                <li class="list-group-item">Dapibus ac facilisis in</li>
                <li class="list-group-item">Morbi leo risus</li>
                <li class="list-group-item">Porta ac consectetur ac</li>
                <li class="list-group-item">Vestibulum at eros</li>
              </ul>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Contextual classes</h4>
            </template>

            <template v-slot:body>
              <p>
                Use contextual classes to style list items with a stateful
                background and color.
              </p>
              <ul class="list-group">
                <li class="list-group-item">Dapibus ac facilisis in</li>
                <li class="list-group-item list-group-item-primary">
                  A simple primary list group item
                </li>
                <li class="list-group-item list-group-item-secondary">
                  A simple secondary list group item
                </li>
                <li class="list-group-item list-group-item-success">
                  A simple success list group item
                </li>
                <li class="list-group-item list-group-item-danger">
                  A simple danger list group item
                </li>
                <li class="list-group-item list-group-item-warning">
                  A simple warning list group item
                </li>
                <li class="list-group-item list-group-item-info">
                  A simple info list group item
                </li>
                <li class="list-group-item list-group-item-light">
                  A simple light list group item
                </li>
                <li class="list-group-item list-group-item-dark">
                  A simple dark list group item
                </li>
              </ul>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">With badges</h4>
            </template>

            <template v-slot:body>
              <p>
                Add badges to any list group item to show unread counts,
                activity, and more with the help of some
                <a href="/docs/4.3/utilities/flex/">utilities</a>.
              </p>
              <ul class="list-group">
                <li
                  class="list-group-item d-flex justify-content-between align-items-center"
                >
                  Cras justo odio
                  <span class="badge badge-primary badge-pill">14</span>
                </li>
                <li
                  class="list-group-item d-flex justify-content-between align-items-center"
                >
                  Dapibus ac facilisis in
                  <span class="badge badge-primary badge-pill">2</span>
                </li>
                <li
                  class="list-group-item d-flex justify-content-between align-items-center"
                >
                  Morbi leo risus
                  <span class="badge badge-primary badge-pill">1</span>
                </li>
              </ul>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">With badges</h4>
            </template>

            <template v-slot:body>
              <p>
                Add badges to any list group item to show unread counts,
                activity, and more with the help of some
                <a href="/docs/4.3/utilities/flex/">utilities</a>.
              </p>
              <ul class="list-group">
                <li
                  class="list-group-item d-flex justify-content-between align-items-center"
                >
                  A list item
                  <span class="badge bg-primary rounded-pill">14</span>
                </li>
                <li
                  class="list-group-item d-flex justify-content-between align-items-center"
                >
                  A second list item
                  <span class="badge bg-primary rounded-pill"
                    >&nbsp;&nbsp;2&nbsp;&nbsp;</span
                  >
                </li>
                <li
                  class="list-group-item d-flex justify-content-between align-items-center"
                >
                  A third list item
                  <span class="badge bg-primary rounded-pill"
                    >&nbsp;&nbsp;1&nbsp;&nbsp;</span
                  >
                </li>
              </ul>
            </template>
          </iq-card>
        </b-col>
        <b-col lg="6" sm="12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">List Active</h4>
            </template>

            <template v-slot:body>
              <p>
                Add <code>.active</code> to a <code>.list-group-item</code> to
                indicate the current active selection.
              </p>
              <!-- Comming Sonn -->
              <ul class="list-group">
                <li class="list-group-item bg-primary">Cras justo odio</li>
                <li class="list-group-item">Dapibus ac facilisis in</li>
                <li class="list-group-item">Morbi leo risus</li>
                <li class="list-group-item">Porta ac consectetur ac</li>
                <li class="list-group-item">Vestibulum at eros</li>
              </ul>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Links and buttons</h4>
            </template>

            <template v-slot:body>
              <p>
                Use <code>&lt;a&gt;</code>s or <code>&lt;button&gt;</code>s to
                create <em>actionable</em> list group items with hover,
                disabled, and active states by adding
                <code>.list-group-item-action</code>. We separate these
                pseudo-classes to ensure list groups made of non-interactive
                elements (like <code>&lt;li&gt;</code>s or
                <code>&lt;div&gt;</code>s) don’t provide a click or tap
                affordance.
              </p>
              <p>
                Be sure to
                <strong
                  >not use the standard <code>.btn</code> classes here</strong
                >.
              </p>
              <!-- Comming Soon -->
              <div class="list-group">
                <a
                  href="#"
                  class="list-group-item list-group-item-action bg-primary"
                >
                  Cras justo odio
                </a>
                <a href="#" class="list-group-item list-group-item-action"
                  >Dapibus ac facilisis in</a
                >
                <a href="#" class="list-group-item list-group-item-action"
                  >Morbi leo risus</a
                >
                <a href="#" class="list-group-item list-group-item-action"
                  >Porta ac consectetur ac</a
                >
                <a
                  href="#"
                  class="list-group-item list-group-item-action disabled"
                  tabindex="-1"
                  aria-disabled="true"
                  >Vestibulum at eros</a
                >
              </div>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Horizontal</h4>
            </template>

            <template v-slot:body>
              <p>
                Add <code>.list-group-horizontal</code> to change the layout of
                list group items from vertical to horizontal across all
                breakpoints. Alternatively, choose a responsive variant
                <code>.list-group-horizontal-{sm|md|lg|xl}</code> to make a list
                group horizontal starting at that breakpoint’s
                <code>min-width</code>. Currently
                <strong
                  >horizontal list groups cannot be combined with flush list
                  groups.</strong
                >
              </p>
              <p>
                <strong>ProTip:</strong> Want equal-width list group items when
                horizontal? Add <code>.flex-fill</code> to each list group item.
              </p>
              <ul class="list-group list-group-horizontal">
                <li class="list-group-item">Cras justo odio</li>
                <li class="list-group-item">Dapibus ac facilisis in</li>
                <li class="list-group-item">Morbi leo risus</li>
              </ul>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Contextual classes Action</h4>
            </template>

            <template v-slot:body>
              <p>
                Use contextual classes to style list items with a stateful
                background and color.
              </p>
              <!-- Comming Soon -->
              <div class="list-group">
                <a href="#" class="list-group-item list-group-item-action"
                  >Dapibus ac facilisis in</a
                >
                <a
                  href="#"
                  class="list-group-item list-group-item-action list-group-item-primary"
                  >A simple primary list group item</a
                >
                <a
                  href="#"
                  class="list-group-item list-group-item-action list-group-item-secondary"
                  >A simple secondary list group item</a
                >
                <a
                  href="#"
                  class="list-group-item list-group-item-action list-group-item-success"
                  >A simple success list group item</a
                >
                <a
                  href="#"
                  class="list-group-item list-group-item-action list-group-item-danger"
                  >A simple danger list group item</a
                >
                <a
                  href="#"
                  class="list-group-item list-group-item-action list-group-item-warning"
                  >A simple warning list group item</a
                >
                <a
                  href="#"
                  class="list-group-item list-group-item-action list-group-item-info"
                  >A simple info list group item</a
                >
                <a
                  href="#"
                  class="list-group-item list-group-item-action list-group-item-light"
                  >A simple light list group item</a
                >
                <a
                  href="#"
                  class="list-group-item list-group-item-action list-group-item-dark"
                  >A simple dark list group item</a
                >
              </div>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Custom Content</h4>
            </template>

            <template v-slot:body>
              <p>
                Add nearly any HTML within, even for linked list groups like the
                one below, with the help of
                <a href="/docs/4.3/utilities/flex/">flexbox utilities</a>.
              </p>
              <!-- Comming Soon -->
              <div class="list-group">
                <a
                  href="#"
                  class="list-group-item list-group-item-action bg-primary"
                >
                  <div class="d-flex w-100 justify-content-between">
                    <h5 class="mb-1 text-white">List group item heading</h5>
                    <small>3 days ago</small>
                  </div>
                  <p class="mb-1">
                    Donec id elit non mi porta gravida at eget metus. Maecenas
                    sed diam eget risus varius blandit.
                  </p>
                  <small>Donec id elit non mi porta.</small>
                </a>
                <a href="#" class="list-group-item list-group-item-action">
                  <div class="d-flex w-100 justify-content-between">
                    <h5 class="mb-1">List group item heading</h5>
                    <small class="text-muted">3 days ago</small>
                  </div>
                  <p class="mb-1">
                    Donec id elit non mi porta gravida at eget metus. Maecenas
                    sed diam eget risus varius blandit.
                  </p>
                  <small class="text-muted">Donec id elit non mi porta.</small>
                </a>
                <a href="#" class="list-group-item list-group-item-action">
                  <div class="d-flex w-100 justify-content-between">
                    <h5 class="mb-1">List group item heading</h5>
                    <small class="text-muted">3 days ago</small>
                  </div>
                  <p class="mb-1">
                    Donec id elit non mi porta gravida at eget metus. Maecenas
                    sed diam eget risus varius blandit.
                  </p>
                  <small class="text-muted">Donec id elit non mi porta.</small>
                </a>
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
  name: "UiListGroup",
  mounted() {
    // socialvue.index()
  },
};
</script>
