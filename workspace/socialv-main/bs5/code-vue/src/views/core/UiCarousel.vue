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
              <h3 class="text-white">Carousel Page</h3>
              <p class="text-white">lorem ipsum</p>
            </div>
          </div>
        </div>
        <div class="col-lg-6 col-sm-12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Slides only</h4>
            </template>

            <template v-slot:body>
              <p>
                Here’s a carousel with slides only. Note the presence of the
                <code>.d-block</code> and <code>.img-fluid</code> on carousel
                images to prevent browser default image alignment.
              </p>
              <!-- Comming Soon -->
              <BCarousel :interval="5000" ride="carousel">
                <BCarouselSlide
                  :img-src="require('@/assets/images/small/img-1.jpg')"
                />
                <BCarouselSlide
                  :img-src="require('@/assets/images/small/img-1.jpg')"
                />
                <BCarouselSlide
                  :img-src="require('@/assets/images/small/img-1.jpg')"
                />
              </BCarousel>
            </template>
          </iq-card>
        </div>
        <div class="col-lg-6 col-sm-12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Slides With Controls</h4>
            </template>

            <template v-slot:body>
              <p>
                Here’s a carousel with slides only. Note the presence of the
                <code>.d-block</code> and <code>.img-fluid</code> on carousel
                images to prevent browser default image alignment.
              </p>
              <BCarousel :interval="5000" ride="carousel" controls>
                <BCarouselSlide
                  :img-src="require('@/assets/images/small/img-1.jpg')"
                />
                <BCarouselSlide
                  :img-src="require('@/assets/images/small/img-1.jpg')"
                />
                <BCarouselSlide
                  :img-src="require('@/assets/images/small/img-1.jpg')"
                />
              </BCarousel>
            </template>
          </iq-card>
        </div>
        <div class="col-lg-6 col-sm-12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Slides With Indicators</h4>
            </template>

            <template v-slot:body>
              <p>
                Here’s a carousel with slides only. Note the presence of the
                <code>.d-block</code> and <code>.img-fluid</code> on carousel
                images to prevent browser default image alignment.
              </p>
              <!-- Comming Soon-->
              <BCarousel indicators :interval="5000" ride="carousel" controls>
                <BCarouselSlide
                  :img-src="require('@/assets/images/small/img-1.jpg')"
                />
                <BCarouselSlide
                  :img-src="require('@/assets/images/small/img-1.jpg')"
                />
                <BCarouselSlide
                  :img-src="require('@/assets/images/small/img-1.jpg')"
                />
              </BCarousel>
            </template>
          </iq-card>
        </div>
        <div class="col-lg-6 col-sm-12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Slides With Captions</h4>
            </template>

            <template v-slot:body>
              <p>
                Here’s a carousel with slides only. Note the presence of the
                <code>.d-block</code> and <code>.img-fluid</code> on carousel
                images to prevent browser default image alignment.
              </p>
              <BCarousel controls indicators :interval="5000" ride="carousel">
                <BCarouselSlide
                  :img-src="require('@/assets/images/small/img-1.jpg')"
                >
                  <h5>First slide label</h5>
                  <p>
                    Some representative placeholder content for the first slide.
                  </p>
                </BCarouselSlide>
                <BCarouselSlide
                  :img-src="require('@/assets/images/small/img-1.jpg')"
                >
                  <h5>Second slide label</h5>
                  <p>
                    Some representative placeholder content for the second
                    slide.
                  </p>
                </BCarouselSlide>
                <BCarouselSlide
                  :img-src="require('@/assets/images/small/img-1.jpg')"
                >
                  <h5>Third slide label</h5>
                  <p>
                    Some representative placeholder content for the third slide.
                  </p>
                </BCarouselSlide>
              </BCarousel>
            </template>
          </iq-card>
        </div>
        <div class="col-lg-6 col-sm-12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Slides With Crossfade</h4>
            </template>

            <template v-slot:body>
              <p>
                Here’s a carousel with slides only. Note the presence of the
                <code>.d-block</code> and <code>.img-fluid</code> on carousel
                images to prevent browser default image alignment.
              </p>
              <BCarousel fade controls>
                <BCarouselSlide
                  :img-src="require('@/assets/images/small/img-1.jpg')"
                />
                <BCarouselSlide
                  :img-src="require('@/assets/images/small/img-1.jpg')"
                />
                <BCarouselSlide
                  :img-src="require('@/assets/images/small/img-1.jpg')"
                />
              </BCarousel>
            </template>
          </iq-card>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
// import { socialvue } from '../../config/pluginInit'
import img1 from "@/assets/images/small/img-1.jpg";

export default {
  name: "UiCarousel",
  data() {
    return {
      check: false,
      manualNavigation: 2,
      img1,
    };
  },
  mounted() {
    // socialvue.index()
  },
  // methods: {
  //   generateImgPath(path) {
  //     return window.origin + process.env.BASE_URL + path;
  //   },
  // },
};
</script>
