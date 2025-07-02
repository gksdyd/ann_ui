<template>
  <div class="content-inner">
    <div class="container">
      <div class="row">
        <div class="col-sm-12">
          <div
            class="card position-relative inner-page-bg bg-primary"
            style="height: 150px"
          >
            <div class="inner-page-title">
              <h3 class="text-white">Embed Video Page</h3>
              <p class="text-white">lorem ipsum</p>
            </div>
          </div>
        </div>
        <div class="col-lg-6 col-sm-12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Embeds Video</h4>
            </template>

            <template v-slot:body>
              <p>
                Wrap any embed like an
                <code class="highlighter-rouge">&lt;iframe&gt;</code> in a
                parent element with
                <code class="highlighter-rouge">.embed-responsive</code> and an
                aspect ratio. The
                <code class="highlighter-rouge">.embed-responsive-item</code>
                isn’t strictly required, but we encourage it.
              </p>

              <div class="ratio ratio-16y9">
                <iframe
                  src="https://www.youtube.com/embed/zpOULjyy-n8?rel=0"
                  title="YouTube video"
                  allowfullscreen
                ></iframe>
              </div>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Responsive Aspect ratios 4:3</h4>
            </template>

            <template v-slot:body>
              <p>
                Progress components are built with two HTML elements, some CSS
                to set the width, and a few attributes.
              </p>

              <div class="ratio ratio-4x3">
                <iframe
                  src="https://www.youtube.com/embed/zpOULjyy-n8?rel=0"
                  title="YouTube video"
                  allowfullscreen
                ></iframe>
              </div>
            </template>
          </iq-card>
        </div>
        <div class="col-lg-6 col-sm-12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Responsive Aspect ratios 21:9</h4>
            </template>

            <template v-slot:body>
              <p>
                Progress components are built with two HTML elements, some CSS
                to set the width, and a few attributes.
              </p>

              <div class="ratio ratio-21x9">
                <iframe
                  src="https://www.youtube.com/embed/zpOULjyy-n8?rel=0"
                  title="YouTube video"
                  allowfullscreen
                ></iframe>
              </div>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Responsive Aspect ratios 1:1</h4>
            </template>

            <template v-slot:body>
              <p>
                Progress components are built with two HTML elements, some CSS
                to set the width, and a few attributes.
              </p>

              <div class="ratio ratio-1x1">
                <iframe
                  src="https://www.youtube.com/embed/zpOULjyy-n8?rel=0"
                  title="YouTube video"
                  allowfullscreen
                ></iframe>
              </div>
            </template>
          </iq-card>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
// import { socialvue } from '../../config/pluginInit'

export default {
  name: "UiEmbedVideo",
  mounted() {
    // socialvue.index()
  },
};
</script>
