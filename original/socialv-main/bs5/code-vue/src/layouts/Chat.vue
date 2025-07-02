<template>
  <Swiper
    tag="ul"
    class="swiper-general messenger-swiper overflow-hidden mb-4"
    :modules="modules"
    :space-between="12"
    :navigation="{
      nextEl: '#similar-products-next',
      prevEl: '#similar-products-prev',
    }"
    :breakpoints="{
      0: {
        slidesPerView: 4.3,
      },
      576: {
        slidesPerView: 4.3,
      },

      768: {
        slidesPerView: 5.3,
      },

      1025: {
        slidesPerView: 7.3,
      },

      1500: {
        slidesPerView: 7.3,
      },
    }"
  >
    <swiper-Slide class="swiper-slide text-center">
      <div class="messanger-box position-relative d-inline-block">
        <img
          src="@/assets/images/chat/avatar/01.png"
          class="avatar-48 object-cover rounded-circle"
          alt="messanger-image"
        />
      </div>
      <p class="mt-2 mb-0 font-size-14 custom-ellipsis text-body">
        Paul Molive
      </p>
    </swiper-Slide>
    <swiper-Slide class="swiper-slide text-center">
      <div class="messanger-box position-relative d-inline-block">
        <img
          src="@/assets/images/chat/avatar/02.png"
          class="avatar-48 object-cover rounded-circle"
          alt="messanger-image"
        />
      </div>
      <p class="mt-2 mb-0 font-size-14 custom-ellipsis text-body">
        John Travolta
      </p>
    </swiper-Slide>
    <swiper-Slide class="swiper-slide text-center">
      <div class="messanger-box position-relative d-inline-block">
        <img
          src="@/assets/images/chat/avatar/03.png"
          class="avatar-48 object-cover rounded-circle"
          alt="messanger-image"
        />
      </div>
      <p class="mt-2 mb-0 font-size-14 custom-ellipsis text-body">Barb Ackue</p>
    </swiper-Slide>
    <swiper-Slide class="swiper-slide text-center">
      <div class="messanger-box position-relative d-inline-block">
        <img
          src="@/assets/images/chat/avatar/04.png"
          class="avatar-48 object-cover rounded-circle"
          alt="messanger-image"
        />
      </div>
      <p class="mt-2 mb-0 font-size-14 custom-ellipsis text-body">Robert Fox</p>
    </swiper-Slide>
    <swiper-Slide class="swiper-slide text-center">
      <div class="messanger-box position-relative d-inline-block">
        <img
          src="@/assets/images/chat/avatar/05.png"
          class="avatar-48 object-cover rounded-circle"
          alt="messanger-image"
        />
      </div>
      <p class="mt-2 mb-0 font-size-14 custom-ellipsis text-body">Maya Didas</p>
    </swiper-Slide>
    <swiper-Slide class="swiper-slide text-center">
      <div class="messanger-box position-relative d-inline-block">
        <img
          src="@/assets/images/chat/avatar/06.png"
          class="avatar-48 object-cover rounded-circle"
          alt="messanger-image"
        />
      </div>
      <p class="mt-2 mb-0 font-size-14 custom-ellipsis text-body">
        Monty Carlo
      </p>
    </swiper-Slide>
    <swiper-Slide class="swiper-slide text-center">
      <div class="messanger-box position-relative d-inline-block">
        <img
          src="@/assets/images/chat/avatar/07.png"
          class="avatar-48 object-cover rounded-circle"
          alt="messanger-image"
        />
      </div>
      <p class="mt-2 mb-0 font-size-14 custom-ellipsis text-body">
        Paige Turner
      </p>
    </swiper-Slide>
    <swiper-Slide class="swiper-slide text-center">
      <div class="messanger-box position-relative d-inline-block">
        <img
          src="@/assets/images/chat/avatar/08.png"
          class="avatar-48 object-cover rounded-circle"
          alt="messanger-image"
        />
      </div>
      <p class="mt-2 mb-0 font-size-14 custom-ellipsis text-body">
        Arnold Schwarzenegger
      </p>
    </swiper-Slide>
    <swiper-Slide class="swiper-slide text-center">
      <div class="messanger-box position-relative d-inline-block">
        <img
          src="@/assets/images/chat/avatar/09.png"
          class="avatar-48 object-cover rounded-circle"
          alt="messanger-image"
        />
      </div>
      <p class="mt-2 mb-0 font-size-14 custom-ellipsis text-body">
        Leonardo DiCaprio
      </p>
    </swiper-Slide>
  </Swiper>
</template>
<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
import { Navigation, Controller } from "swiper";
import { ref } from "vue";

const modules = [Navigation, Controller];
const items1 = [
  { images: require("@/assets/images/store/product-detail/01.jpg") },
  { images: require("@/assets/images/store/product-detail/01.jpg") },
  { images: require("@/assets/images/store/product-detail/01.jpg") },
  { images: require("@/assets/images/store/product-detail/01.jpg") },
  { images: require("@/assets/images/store/product-detail/01.jpg") },
];
const items2 = [
  { images: require("@/assets/images/store/product-detail/01.jpg") },
  { images: require("@/assets/images/store/product-detail/01.jpg") },
  { images: require("@/assets/images/store/product-detail/01.jpg") },
  { images: require("@/assets/images/store/product-detail/01.jpg") },
  { images: require("@/assets/images/store/product-detail/01.jpg") },
];
const mainSwiper = ref(null);
const thumbSwiper = ref(null);
const setMainSwiper = (swiper) => {
  mainSwiper.value = swiper;
};
const setThumbSwiper = (swiper) => {
  thumbSwiper.value = swiper;
};
</script>
