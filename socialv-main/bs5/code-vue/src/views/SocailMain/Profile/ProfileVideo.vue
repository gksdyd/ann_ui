<template>
  <div class="content-inner">
    <div class="container">
      <div class="row">
        <div
          v-for="(item, index) in items"
          :key="index"
          class="col-lg-4 col-md-6"
          @click="($event) => (toggler = !toggler)"
        >
          <div class="card">
            <div class="card-body card-thumbnail p-0">
              <div
                class="position-relative iq-video-hover user-images position-relative overflow-hidden"
              >
                <a :data-fslightbox="'html5-video-' + index">
                  <img
                    :src="item.imageSource"
                    class="img-fluid rounded"
                    alt="file-manager"
                    loading="lazy"
                  />
                </a>
                <div class="image-hover-data">
                  <div class="product-elements-icon">
                    <ul class="d-flex align-items-center m-0 p-0 list-inline">
                      <li>
                        <a
                          href="#"
                          class="pe-3 text-white d-flex align-items-center"
                        >
                          {{ item.likes }}
                          <i class="material-symbols-outlined md-14 ms-1"
                            >thumb_up</i
                          >
                        </a>
                      </li>
                      <li>
                        <a
                          href="#"
                          class="pe-3 text-white d-flex align-items-center"
                        >
                          {{ item.comments }}
                          <span class="material-symbols-outlined md-14 ms-1"
                            >chat_bubble_outline</span
                          >
                        </a>
                      </li>
                      <li>
                        <a
                          href="#"
                          class="pe-3 text-white d-flex align-items-center"
                        >
                          {{ item.shares }}
                          <span class="material-symbols-outlined md-14 ms-1"
                            >forward</span
                          >
                        </a>
                      </li>
                    </ul>
                  </div>
                </div>
                <a
                  href="#"
                  class="image-edit-btn material-symbols-outlined md-16"
                  v-b-tooltip.hover="'Edit or Remove'"
                >
                  drive_file_rename_outline
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <FsLightbox
    :toggler="toggler"
    :sources="[
      require('@/assets/images/plugins/video-2.mp4'),
      require('@/assets/images/plugins/video-3.mp4'),
      require('@/assets/images/plugins/video-1.mp4'),
      require('@/assets/images/plugins/video-3.mp4'),
      require('@/assets/images/plugins/video-1.mp4'),
      require('@/assets/images/plugins/video-1.mp4'),
      require('@/assets/images/plugins/video-1.mp4'),
      require('@/assets/images/plugins/video-1.mp4'),
      require('@/assets/images/plugins/video-1.mp4'),
      require('@/assets/images/plugins/video-1.mp4'),
      require('@/assets/images/plugins/video-1.mp4'),
      require('@/assets/images/plugins/video-1.mp4'),
      require('@/assets/images/plugins/video-1.mp4'),
      require('@/assets/images/plugins/video-1.mp4'),
      require('@/assets/images/plugins/video-1.mp4'),
    ]"
  />
</template>
<script>
// import { socialvue } from '../../../config/pluginInit'
import FsLightbox from "fslightbox-vue/v3";
export default {
  name: "ProfileVideo",
  components: {
    FsLightbox,
  },
  data() {
    return {
      toggler: false,
      items: [
        {
          imageSource: require("@/assets/images/page-img/54.jpg"),
          likes: 60,
          comments: 30,
          shares: 10,
        },
        {
          imageSource: require("@/assets/images/page-img/51.jpg"),
          likes: 80,
          comments: 45,
          shares: 15,
        },
        {
          imageSource: require("@/assets/images/page-img/52.jpg"),
          likes: 50,
          comments: 25,
          shares: 8,
        },
        {
          imageSource: require("@/assets/images/page-img/55.jpg"),
          likes: 50,
          comments: 25,
          shares: 8,
        },
        {
          imageSource: require("@/assets/images/page-img/56.jpg"),
          likes: 50,
          comments: 25,
          shares: 8,
        },
        {
          imageSource: require("@/assets/images/page-img/57.jpg"),
          likes: 50,
          comments: 25,
          shares: 8,
        },
        {
          imageSource: require("@/assets/images/page-img/58.jpg"),
          likes: 50,
          comments: 25,
          shares: 8,
        },
        {
          imageSource: require("@/assets/images/page-img/60.jpg"),
          likes: 50,
          comments: 25,
          shares: 8,
        },
        {
          imageSource: require("@/assets/images/page-img/59.jpg"),
          likes: 50,
          comments: 25,
          shares: 8,
        },
        {
          imageSource: require("@/assets/images/page-img/51.jpg"),
          likes: 50,
          comments: 25,
          shares: 8,
        },
        {
          imageSource: require("@/assets/images/page-img/52.jpg"),
          likes: 50,
          comments: 25,
          shares: 8,
        },
        {
          imageSource: require("@/assets/images/page-img/53.jpg"),
          likes: 50,
          comments: 25,
          shares: 8,
        },
        {
          imageSource: require("@/assets/images/page-img/54.jpg"),
          likes: 50,
          comments: 25,
          shares: 8,
        },
        {
          imageSource: require("@/assets/images/page-img/55.jpg"),
          likes: 50,
          comments: 25,
          shares: 8,
        },
        {
          imageSource: require("@/assets/images/page-img/56.jpg"),
          likes: 50,
          comments: 25,
          shares: 8,
        },
      ],
    };
  },
};
</script>
