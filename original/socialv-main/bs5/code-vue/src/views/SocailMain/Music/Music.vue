<template>
  <div class="content-inner">
    <b-container>
      <b-row>
        <b-col md="4">
          <b-card no-body class="card-block card-stretch card-height">
            <div class="card-header d-flex justify-content-between">
              <div class="header-title">
                <h4 class="card-title">Play Lists</h4>
              </div>
            </div>
            <b-card-body class="pt-0">
              <ul class="music-lists m-0 p-0">
                <li
                  :class="`d-flex ${item.mbclass} align-items-center`"
                  v-for="(item, index) in musicData"
                  :key="index"
                >
                  <div class="user-img img-fluid">
                    <img
                      :src="item.img"
                      alt="story-img"
                      class="rounded-circle avatar-40"
                    />
                  </div>
                  <div class="d-flex justify-content-between w-100">
                    <div class="ms-3">
                      <h6>{{ item.heading }}</h6>
                    </div>
                    <div class="music-time">{{ item.time }}</div>
                  </div>
                </li>
              </ul>
            </b-card-body>
          </b-card>
        </b-col>
        <b-col md="8">
          <b-card no-body class="card-block card-stretch card-height">
            <b-card-body class="p-0">
              <a href="#"
                ><img
                  src="../../../assets/images/page-img/48.jpg"
                  alt="story-img"
                  class="img-fluid rounded h-100 w-100"
              /></a>
            </b-card-body>
          </b-card>
        </b-col>
        <b-col sm="12">
          <b-card no-body class="card-block card-stretch card-height">
            <div class="card-header d-flex justify-content-between">
              <div class="header-title">
                <h4 class="card-title">New Music</h4>
              </div>
              <div class="card-header-toolbar d-flex align-items-center">
                <a href="#">View All</a>
              </div>
            </div>
            <b-card-body class="pt-0">
              <Swiper
                tag="ul"
                class="d-flex list-inline m-0 p-0"
                :modules="modules"
                :space-between="16"
                :loop="true"
                :slide-per-view="5"
                :navigation="{
                  nextEl: '#similar-products-next',
                  prevEl: '#similar-products-prev',
                }"
                :breakpoints="{
                  320: { slidesPerView: 1 },
                  550: { slidesPerView: 3 },
                  991: { slidesPerView: 3 },
                  1400: { slidesPerView: 5 },
                  1500: { slidesPerView: 5 },
                  1920: { slidesPerView: 5 },
                  2040: { slidesPerView: 5 },
                  2440: { slidesPerView: 5 },
                }"
              >
                <SwiperSlide
                  class="text-center col-md-12"
                  v-for="(newmusic, index) in newMusic"
                  :key="index"
                >
                  <div class="music-thumbnail position-relative mb-3">
                    <a href="#"
                      ><img
                        :src="newmusic.img"
                        alt="music-thumb"
                        class="img-fluid w-100"
                    /></a>
                    <div class="play-btn">
                      <a href="#" class="material-symbols-outlined text-white"
                        >play_arrow</a
                      >
                    </div>
                  </div>
                  <h6>{{ newmusic.name }}</h6>
                  <p class="mb-0">Best Advice</p>
                </SwiperSlide>
              </Swiper>
            </b-card-body>
          </b-card>
        </b-col>
        <b-col sm="12">
          <b-card no-body class="card-block card-stretch card-height">
            <div class="card-header d-flex justify-content-between">
              <div class="header-title">
                <h4 class="card-title">Recent Added</h4>
              </div>
              <div class="card-header-toolbar d-flex align-items-center">
                <a href="#">View All</a>
              </div>
            </div>
            <b-card-body class="pt-0">
              <Swiper
                tag="ul"
                class="d-flex list-inline m-0 p-0"
                :modules="modules"
                :space-between="16"
                :loop="true"
                :slide-per-view="5"
                :navigation="{
                  nextEl: '#similar-products-next',
                  prevEl: '#similar-products-prev',
                }"
                :breakpoints="{
                  320: { slidesPerView: 1 },
                  550: { slidesPerView: 3 },
                  991: { slidesPerView: 3 },
                  1400: { slidesPerView: 5 },
                  1500: { slidesPerView: 5 },
                  1920: { slidesPerView: 5 },
                  2040: { slidesPerView: 5 },
                  2440: { slidesPerView: 5 },
                }"
              >
                <SwiperSlide
                  class="text-center col-md-12"
                  v-for="(recent, index) in recentAdded"
                  :key="index"
                >
                  <div class="music-thumbnail position-relative mb-3">
                    <a href="#"
                      ><img
                        :src="recent.img"
                        alt="music-thumb"
                        class="img-fluid w-100"
                    /></a>
                    <div class="play-btn">
                      <a href="#" class="material-symbols-outlined text-white"
                        >play_arrow</a
                      >
                    </div>
                  </div>
                  <h6>{{ recent.heading }}</h6>
                  <p class="mb-0">Best Advice</p>
                </SwiperSlide>
              </Swiper>
            </b-card-body>
          </b-card>
        </b-col>
        <b-col sm="12">
          <b-card no-body class="card-block card-stretch card-height">
            <div class="card-header d-flex justify-content-between">
              <div class="header-title">
                <h4 class="card-title">Top Music</h4>
              </div>
              <div class="card-header-toolbar d-flex align-items-center">
                <a href="#">View All</a>
              </div>
            </div>
            <b-card-body class="pt-0">
              <Swiper
                tag="ul"
                class="d-flex list-inline m-0 p-0"
                :modules="modules"
                :dir="ltr"
                :space-between="16"
                :loop="true"
                :slide-per-view="5"
                :navigation="{
                  nextEl: '#similar-products-next',
                  prevEl: '#similar-products-prev',
                }"
                :breakpoints="{
                  320: { slidesPerView: 1 },
                  550: { slidesPerView: 3 },
                  991: { slidesPerView: 3 },
                  1400: { slidesPerView: 5 },
                  1500: { slidesPerView: 5 },
                  1920: { slidesPerView: 5 },
                  2040: { slidesPerView: 5 },
                  2440: { slidesPerView: 5 },
                }"
              >
                <SwiperSlide
                  class="text-center col-md-12"
                  v-for="(music, index) in topMusic"
                  :key="index"
                >
                  <div class="music-thumbnail position-relative mb-3">
                    <a href="#"
                      ><img
                        :src="music.img"
                        alt="music-thumb"
                        class="img-fluid w-100"
                    /></a>
                    <div class="play-btn">
                      <a href="#" class="material-symbols-outlined text-white"
                        >play_arrow</a
                      >
                    </div>
                  </div>
                  <h6>{{ music.heading }}</h6>
                  <p class="mb-0">Best Advice</p>
                </SwiperSlide>
              </Swiper>
            </b-card-body>
          </b-card>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>
<script setup>
import { ref } from "vue";
import { Swiper, SwiperSlide } from "swiper/vue";
// import { Navigation, Controller } from 'swiper'
import "swiper/scss";

const musicData = ref([
  {
    img: require("../../../assets/images/page-img/l1.jpg"),
    heading: "Ember",
    time: "3:00",
    mbclass: "mb-4",
  },
  {
    img: require("../../../assets/images/page-img/l2.jpg"),
    heading: "Light Out(Bonus Track)",
    time: "5:00",
    mbclass: "mb-4",
  },
  {
    img: require("../../../assets/images/page-img/l3.jpg"),
    heading: "Darkness Overture",
    time: "2:30",
    mbclass: "mb-4",
  },
  {
    img: require("../../../assets/images/page-img/l4.jpg"),
    heading: "Dritin",
    time: "4:20",
    mbclass: "mb-4",
  },
  {
    img: require("../../../assets/images/page-img/l5.jpg"),
    heading: "Bones",
    time: "1:45",
    mbclass: "mb-4",
  },
  {
    img: require("../../../assets/images/page-img/l6.jpg"),
    heading: "Hozier",
    time: "2:00",
    mbclass: "mb-0",
  },
]);

const newMusic = ref([
  {
    img: require("../../../assets/images/page-img/n1.jpg"),
    name: "Sean Paul",
  },
  {
    img: require("../../../assets/images/page-img/n2.jpg"),
    name: "Fetty Wap",
  },
  {
    img: require("../../../assets/images/page-img/n3.jpg"),
    name: "Brittany Howard",
  },
  {
    img: require("../../../assets/images/page-img/n4.jpg"),
    name: "Elton John",
  },
  {
    img: require("../../../assets/images/page-img/n5.jpg"),
    name: "Tierra Whack",
  },
  {
    img: require("../../../assets/images/page-img/n6.jpg"),
    name: "Trippie Redd",
  },
  {
    img: require("../../../assets/images/page-img/n7.jpg"),
    name: "Quincy Jones",
  },
  {
    img: require("../../../assets/images/page-img/n8.jpg"),
    name: "Ciara",
  },
]);

const recentAdded = ref([
  {
    img: require("../../../assets/images/page-img/n8.jpg"),
    heading: "Lizzo",
  },
  {
    img: require("../../../assets/images/page-img/r8.jpg"),
    heading: "Kathleen Hanna",
  },
  {
    img: require("../../../assets/images/page-img/n7.jpg"),
    heading: "Sheryl Crow",
  },
  {
    img: require("../../../assets/images/page-img/r1.jpg"),
    heading: "Karen O",
  },
  {
    img: require("../../../assets/images/page-img/n1.jpg"),
    heading: "Cyndi Lauper",
  },
  {
    img: require("../../../assets/images/page-img/r2.jpg"),
    heading: "Rick Ross",
  },
  {
    img: require("../../../assets/images/page-img/r7.jpg"),
    heading: "Kamasi Washington",
  },
  {
    img: require("../../../assets/images/page-img/n2.jpg"),
    heading: "Christina Aguilera",
  },
]);

const topMusic = ref([
  {
    img: require("../../../assets/images/page-img/r1.jpg"),
    heading: "Mary J. Blige",
  },
  {
    img: require("../../../assets/images/page-img/r2.jpg"),
    heading: "Ne-Yo",
  },
  {
    img: require("../../../assets/images/page-img/r3.jpg"),
    heading: "Annie Flook",
  },
  {
    img: require("../../../assets/images/page-img/r4.jpg"),
    heading: "Karen O",
  },
  {
    img: require("../../../assets/images/page-img/r5.jpg"),
    heading: "Alex Gvojic",
  },
  {
    img: require("../../../assets/images/page-img/r6.jpg"),
    heading: "Mindy Monk",
  },
  {
    img: require("../../../assets/images/page-img/r7.jpg"),
    heading: "Coffey Rock",
  },
  {
    img: require("../../../assets/images/page-img/r8.jpg"),
    heading: "Sam Smith",
  },
]);

const newoptions = {
  centeredSlides: false,
  loop: false,
  slidesPerView: 5,
  autoplay: {
    delay: 3000,
  },
  spaceBetween: 15,
  breakpoints: {
    320: {
      slidesPerView: 1,
    },
    550: {
      slidesPerView: 2,
    },
    768: {
      slidesPerView: 3,
    },
    1199: {
      slidesPerView: 4,
    },
    1400: {
      slidesPerView: 5,
    },
  },
  pagination: {
    el: ".swiper-pagination",
  },
  navigation: {
    nextEl: ".swiper-button-next",
    prevEl: ".swiper-button-prev",
  },
  scrollbar: {
    el: ".swiper-scrollbar",
  },
};

const recentoptions = {
  centeredSlides: false,
  loop: false,
  slidesPerView: 5,
  autoplay: {
    delay: 3000,
  },
  spaceBetween: 15,
  breakpoints: {
    320: {
      slidesPerView: 1,
    },
    550: {
      slidesPerView: 2,
    },
    768: {
      slidesPerView: 3,
    },
    1199: {
      slidesPerView: 4,
    },
    1400: {
      slidesPerView: 5,
    },
  },
  pagination: {
    el: ".swiper-pagination",
  },
  navigation: {
    nextEl: ".swiper-button-next",
    prevEl: ".swiper-button-prev",
  },
  scrollbar: {
    el: ".swiper-scrollbar",
  },
};
const topoptions = {
  centeredSlides: false,
  loop: false,
  slidesPerView: 5,
  autoplay: {
    delay: 3000,
  },
  spaceBetween: 15,
  breakpoints: {
    320: {
      slidesPerView: 1,
    },
    550: {
      slidesPerView: 2,
    },
    768: {
      slidesPerView: 3,
    },
    1199: {
      slidesPerView: 4,
    },
    1400: {
      slidesPerView: 5,
    },
  },
  pagination: {
    el: ".swiper-pagination",
  },
  navigation: {
    nextEl: ".swiper-button-next",
    prevEl: ".swiper-button-prev",
  },
  scrollbar: {
    el: ".swiper-scrollbar",
  },
};
</script>
