<template>
  <section class="sign-in-page">
    <div class="container-fluid">
      <div class="row align-items-center">
        <div class="col-md-6 overflow-hidden position-relative">
          <div
            class="bg-primary w-100 h-100 position-absolute top-0 bottom-0 start-0 end-0"
          ></div>
          <div class="container-inside z-1">
            <div class="main-circle circle-small"></div>
            <div class="main-circle circle-medium"></div>
            <div class="main-circle circle-large"></div>
            <div class="main-circle circle-xlarge"></div>
            <div class="main-circle circle-xxlarge"></div>
          </div>
          <div class="sign-in-detail container-inside-top">
            <router-link
              to="/"
              class="d-inline-flex align-items-center justify-content-center gap-2 text-white mb-4"
            >
              <svg
                width="50"
                viewBox="0 0 24 24"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  fill-rule="evenodd"
                  clip-rule="evenodd"
                  d="M1.67733 9.50001L7.88976 20.2602C9.81426 23.5936 14.6255 23.5936 16.55 20.2602L22.7624 9.5C24.6869 6.16666 22.2813 2 18.4323 2H6.00746C2.15845 2 -0.247164 6.16668 1.67733 9.50001ZM14.818 19.2602C13.6633 21.2602 10.7765 21.2602 9.62181 19.2602L9.46165 18.9828L9.46597 18.7275C9.48329 17.7026 9.76288 16.6993 10.2781 15.8131L12.0767 12.7195L14.1092 16.2155C14.4957 16.8803 14.7508 17.6132 14.8607 18.3743L14.9544 19.0239L14.818 19.2602ZM16.4299 16.4683L19.3673 11.3806C18.7773 11.5172 18.172 11.5868 17.5629 11.5868H13.7316L15.8382 15.2102C16.0721 15.6125 16.2699 16.0335 16.4299 16.4683ZM20.9542 8.63193L21.0304 8.5C22.1851 6.5 20.7417 4 18.4323 4H17.8353L17.1846 4.56727C16.6902 4.99824 16.2698 5.50736 15.9402 6.07437L13.8981 9.58676H17.5629C18.4271 9.58676 19.281 9.40011 20.0663 9.03957L20.9542 8.63193ZM14.9554 4C14.6791 4.33499 14.4301 4.69248 14.2111 5.06912L12.0767 8.74038L10.0324 5.22419C9.77912 4.78855 9.48582 4.37881 9.15689 4H14.9554ZM6.15405 4H6.00746C3.69806 4 2.25468 6.50001 3.40938 8.50001L3.4915 8.64223L4.37838 9.04644C5.15962 9.40251 6.00817 9.58676 6.86672 9.58676H10.2553L8.30338 6.22943C7.9234 5.57587 7.42333 5.00001 6.8295 4.53215L6.15405 4ZM5.07407 11.3833L7.88909 16.2591C8.05955 15.7565 8.28025 15.2702 8.54905 14.8079L10.4218 11.5868H6.86672C6.26169 11.5868 5.66037 11.5181 5.07407 11.3833Z"
                  fill="currentColor"
                ></path>
              </svg>
              <h2
                class="logo-title fw-semibold text-white"
                data-setting="app_name"
              >
                SocialV
              </h2>
            </router-link>
            <Swiper
              :options="options"
              class="swiper-general list-inline m-0 p-0"
            >
              <SwiperSlide>
                <img
                  src="@/assets/images/login/1.jpg"
                  class="signin-img img-fluid mb-5 rounded-3"
                  alt="logo"
                />
                <h2 class="mb-3 text-white fw-semibold">
                  Power UP Your Friendship
                </h2>
                <p class="font-size-16 text-white mb-0">
                  It is a long established fact that a reader will be <br />
                  distracted by the readable content.
                </p>
              </SwiperSlide>
              <SwiperSlide>
                <img
                  src="@/assets/images/login/2.jpg"
                  class="signin-img img-fluid mb-5 rounded-3"
                  alt="logo"
                />
                <h2 class="mb-3 text-white fw-semibold">
                  Connect with the world
                </h2>
                <p class="font-size-16 text-white mb-0">
                  It is a long established fact that a reader will be <br />
                  distracted by the readable content.
                </p>
              </SwiperSlide>
              <SwiperSlide>
                <img
                  src="@/assets/images/login/3.jpg"
                  class="signin-img img-fluid mb-5 rounded-3"
                  alt="logo"
                />
                <h2 class="mb-3 text-white fw-semibold">Together Is better</h2>
                <p class="font-size-16 text-white mb-0">
                  It is a long established fact that a reader will be<br />
                  distracted by the readable content.
                </p>
              </SwiperSlide>
            </Swiper>
          </div>
        </div>
        <div class="col-md-6">
          <div class="sign-in-from">
            <img
              src="@/assets/images/user/1.jpg"
              alt="user-image"
              class="rounded-circle"
            />
            <h4 class="mt-3 mb-0">Hi ! Michael Smith</h4>
            <p>Enter your password to access the admin.</p>
            <form class="mt-5" @submit.prevent="onSubmit()">
              <div class="form-group text-start mb-0">
                <label class="form-label fw-bold h6" for="exampleInputEmail1"
                  >Your Password</label
                >
                <input
                  type="Password"
                  class="form-control mb-0"
                  id="exampleInputEmail1"
                  placeholder="Your Full Name"
                />
              </div>
              <div class="d-inline-block w-100">
                <button
                  type="submit"
                  class="btn btn-primary mt-4 fw-semibold text-uppercase letter-spacing-1"
                >
                  Log In
                </button>
              </div>
            </form>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- <section class="sign-in-page">
  <div id="container-inside">
    <div id="circle-small"></div>
    <div id="circle-medium"></div>
    <div id="circle-large"></div>
    <div id="circle-xlarge"></div>
    <div id="circle-xxlarge"></div>
  </div>
  <div class="container p-0">
    <div class="row no-gutters">
      <div class="col-md-6 text-center pt-5">
        <div class="sign-in-detail text-white">
          <a class="sign-in-logo mb-5" href="#"><img src="@/assets/images/logo-full.png" class="img-fluid" alt="logo"></a>
          <Swiper :options="options">
            <SwiperSlide  class="item">
              <img src="@/assets/images/login/1.png" class="img-fluid mb-4" alt="logo">
              <h4 class="mb-1 text-white">Manage your orders</h4>
              <p>It is a long established fact that a reader will be distracted by the readable content.</p>
            </SwiperSlide>
            <SwiperSlide class="item">
              <img src="@/assets/images/login/2.png" class="img-fluid mb-4" alt="logo">
              <h4 class="mb-1 text-white">Manage your orders</h4>
              <p>It is a long established fact that a reader will be distracted by the readable content.</p>
            </SwiperSlide>
            <SwiperSlide class="item">
              <img src="@/assets/images/login/3.png" class="img-fluid mb-4" alt="logo">
              <h4 class="mb-1 text-white">Manage your orders</h4>
              <p>It is a long established fact that a reader will be distracted by the readable content.</p>
            </SwiperSlide>
          </Swiper>
        </div>
      </div>
      <div class="col-md-6 bg-white pt-5 pt-5 pb-lg-0 pb-5">
        <div class="sign-in-from">
          <img src="@/assets/images/user/1.jpg" alt="user-image" class="rounded-circle">
          <h4 class="mt-3 mb-0">Hi ! Michael Smith</h4>
          <p>Enter your password to access the admin.</p>
          <form class="mt-4" @submit.prevent="onSubmit()">
            <div class="form-group">
                     <label class="form-label" for="exampleInputEmail1">Password</label>
                     <input type="Password" class="form-control mb-0" id="exampleInputEmail1"  placeholder="Password">
                  </div>
                  <div class="d-inline-block w-100">
                     <button type="submit" class="btn btn-primary float-right">Log In</button>
                  </div>
          </form>
        </div>
      </div>
    </div>
  </div>
</section> -->
</template>
<script>
import Swiper from "../../../components/custom/slider/Swiper";
import SwiperSlide from "../../../components/custom/slider/SwiperSlide";
export default {
  name: "LockScreen1",
  components: { Swiper, SwiperSlide },
  data() {
    return {
      options: {
        centeredSlides: false,
        loop: true,
        slidesPerView: 1,
        autoplay: {
          delay: 3000,
        },
        spaceBetween: 15,
        pagination: {
          el: ".swiper-pagination",
        },
        navigation: {
          nextEl: ".swiper-button-next",
          prevEl: ".swiper-button-prev",
        },

        // And if we need scrollbar
        scrollbar: {
          el: ".swiper-scrollbar",
        },
      },
    };
  },
  methods: {
    onSubmit() {
      this.$router.push({ name: "social.list" });
    },
  },
};
</script>
