<template>
  <div class="content-inner">
    <div class="container p-0">
      <div class="row no-gutters vh-100">
        <div class="col-12 text-center align-self-center">
          <div class="iq-error position-relative mt-5">
            <img
              :src="errorImgLight"
              class="img-fluid iq-error-img img-light center"
              alt="light image"
            />
            <img
              :src="image404"
              class="img-fluid iq-error-img img-dark center"
              alt="dark image"
            />
            <h2 class="mb-0 text-center">Oops! This Page is Not Found.</h2>
            <p class="text-center">The requested page dose not exist.</p>
            <a href="#" @click="$router.go(-1)" class="btn btn-primary mt-3"
              ><span class="d-flex align-items-center">
                <i class="material-symbols-outlined md-18 me-1">home</i>Back to
                Home</span
              ></a
            >
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
// import { socialvue } from '../../config/pluginInit'

export default {
  name: "Error404",
  mounted() {
    // socialvue.index()
    // const body = document.querySelector('body')
    // body.classList.add('iq-bg-primary')
  },
  data() {
    return {
      errorImgLight: require("../../assets/images/error/404-light.png"),
      image404: require("../../assets/images/error/404.png"),
    };
  },
};
</script>
