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
              <h3 class="text-white">Typography Page</h3>
              <p class="text-white">lorem ipsum</p>
            </div>
          </b-card>
        </b-col>
        <b-col sm="12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Display headings</h4>
            </template>
            <template v-slot:body>
              <p>
                Traditional heading elements are designed to work best in the
                meat of your page content. When you need a heading to stand out,
                consider using a <strong>display heading</strong>—a larger,
                slightly more opinionated heading style. Keep in mind these
                headings are not responsive by default, but it’s possible to
                enable
                <a href="https://getbootstrap.com/" target="_blank"
                  >responsive font sizes</a
                >.
              </p>

              <h1 class="display-1">Display</h1>
              <h1 class="display-2">Display</h1>
              <h1 class="display-3">Display</h1>
              <h1 class="display-4">Display</h1>
              <h1 class="display-5">Display</h1>
              <h1 class="display-6 mb-0">Display</h1>
            </template>
          </iq-card>
        </b-col>
        <b-col lg="6" sm="12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Typography</h4>
            </template>

            <b-card-body class="pt-0">
              <p>
                All HTML headings, <code>&lt;h1&gt;</code> through
                <code>&lt;h6&gt;</code>, are available.
              </p>

              <h1>h1. Bootstrap heading</h1>
              <h2>h2. Bootstrap heading</h2>
              <h3>h3. Bootstrap heading</h3>
              <h4>h4. Bootstrap heading</h4>
              <h5>h5. Bootstrap heading</h5>
              <h6 class="mb-0">h6. Bootstrap heading</h6>
            </b-card-body>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Inline text elements</h4>
            </template>
            <template v-slot:body>
              <p>Styling for common inline HTML5 elements.</p>
              <p>You can use the mark tag to <mark>highlight</mark> text.</p>
              <p>
                <del
                  >This line of text is meant to be treated as deleted
                  text.</del
                >
              </p>
              <p>
                <s
                  >This line of text is meant to be treated as no longer
                  accurate.</s
                >
              </p>
              <p>
                <ins
                  >This line of text is meant to be treated as an addition to
                  the document.</ins
                >
              </p>
              <p><u>This line of text will render as underlined</u></p>
              <p>
                <small
                  >This line of text is meant to be treated as fine
                  print.</small
                >
              </p>
              <p><strong>This line rendered as bold text.</strong></p>
              <p><em>This line rendered as italicized text.</em></p>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Lists Inline</h4>
            </template>
            <template v-slot:body>
              <p>
                Remove a list’s bullets and apply some light
                <code>margin</code> with a combination of two classes,
                <code>.list-inline</code> and <code>.list-inline-item</code>.
              </p>
              <ul class="list-inline">
                <li class="list-inline-item">Lorem ipsum</li>
                <li class="list-inline-item ms-1">Phasellus iaculis</li>
                <li class="list-inline-item ms-1">Nulla volutpat</li>
              </ul>
            </template>
          </iq-card>
        </b-col>
        <b-col lg="6" sm="12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Headings</h4>
            </template>
            <template v-slot:body>
              <p>
                <code>.h1</code> through <code>.h6</code> classes are also
                available, for when you want to match the font styling of a
                heading but cannot use the associated HTML element.
              </p>
              <p class="h1 mb-3">h1. Bootstrap heading</p>
              <p class="h2 mb-3">h2. Bootstrap heading</p>
              <p class="h3 mb-3">h3. Bootstrap heading</p>
              <p class="h4 mb-3">h4. Bootstrap heading</p>
              <p class="h5 mb-3">h5. Bootstrap heading</p>
              <p class="h6 mb-0">h6. Bootstrap heading</p>
            </template>
          </iq-card>
          <iq-card body-class="'pt-0'">
            <template v-slot:headerTitle>
              <h4 class="card-title">Lists Unstyled</h4>
            </template>
            <b-card-body class="pt-0">
              <p>
                Remove the default <code>list-style</code> and left margin on
                list items (immediate children only).
                <strong
                  >This only applies to immediate children list items</strong
                >, meaning you will need to add the class for any nested lists
                as well.
              </p>
              <ul class="list-unstyled">
                <li>Lorem ipsum dolor sit amet</li>
                <li>Consectetur adipiscing elit</li>
                <li>Integer molestie lorem at massa</li>
                <li>Facilisis in pretium nisl aliquet</li>
                <li>
                  Nulla volutpat aliquam velit
                  <ul>
                    <li>Phasellus iaculis neque</li>
                    <li>Purus sodales ultricies</li>
                    <li>Vestibulum laoreet porttitor sem</li>
                    <li>Ac tristique libero volutpat at</li>
                  </ul>
                </li>
                <li>Faucibus porta lacus fringilla vel</li>
                <li>Aenean sit amet erat nunc</li>
                <li>Eget porttitor lorem</li>
              </ul>
            </b-card-body>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Blockquotes</h4>
            </template>
            <template v-slot:body>
              <p>
                For quoting blocks of content from another source within your
                document. Wrap
                <code>&lt;blockquote class="blockquote"&gt;</code> around any
                <abbr title="HyperText Markup Language">HTML</abbr> as the
                quote.
              </p>
              <blockquote class="blockquote">
                <p class="mb-0">
                  Lorem ipsum dolor sit amet, consectetur adipiscing elit.
                  Integer posuere erat a ante.
                </p>
                <footer class="blockquote-footer mt-0">
                  Someone famous in
                  <cite title="Source Title">Source Title</cite>
                </footer>
              </blockquote>
            </template>
          </iq-card>
        </b-col>
        <b-col sm="12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Description list alignment</h4>
            </template>

            <template v-slot:body>
              <p>
                Align terms and descriptions horizontally by using our grid
                system’s predefined classes (or semantic mixins). For longer
                terms, you can optionally add a
                <code>.text-truncate</code> class to truncate the text with an
                ellipsis.
              </p>
              <dl class="row">
                <dt class="col-sm-3">Description lists</dt>
                <dd class="col-sm-9">
                  A description list is perfect for defining terms.
                </dd>
                <dt class="col-sm-3">Euismod</dt>
                <dd class="col-sm-9">
                  <p class="mb-0">
                    Vestibulum id ligula porta felis euismod semper eget lacinia
                    odio sem nec elit.
                  </p>
                  <p class="mb-0">
                    Donec id elit non mi porta gravida at eget metus.
                  </p>
                </dd>
                <dt class="col-sm-3">Malesuada porta</dt>
                <dd class="col-sm-9">
                  Etiam porta sem malesuada magna mollis euismod.
                </dd>
                <dt class="col-sm-3 text-truncate">
                  Truncated term is truncated
                </dt>
                <dd class="col-sm-9">
                  Fusce dapibus, tellus ac cursus commodo, tortor mauris
                  condimentum nibh, ut fermentum massa justo sit amet risus.
                </dd>
                <dt class="col-sm-3">Nesting</dt>
                <dd class="col-sm-9">
                  <dl class="row">
                    <dt class="col-sm-4">Nested definition list</dt>
                    <dd class="col-sm-8">
                      Aenean posuere, tortor sed cursus feugiat, nunc augue
                      blandit nunc.
                    </dd>
                  </dl>
                </dd>
              </dl>
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
  name: "UiTypography",
  mounted() {
    // socialvue.index()
  },
};
</script>
