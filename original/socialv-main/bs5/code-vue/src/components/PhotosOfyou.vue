<template>
  <div class="d-grid gap-2 d-grid-template-1fr-13">
    <div
      v-for="(item, index) in profileImages"
      :key="index"
      @click="($event) => (toggler = !toggler)"
    >
      <div class="user-images position-relative overflow-hidden">
        <a data-fslightbox="gallery">
          <img
            :src="item.img"
            alt="Responsive image"
            class="img-fluid rounded"
            loading="lazy"
          />
        </a>
        <div class="image-hover-data">
          <div class="product-elements-icon">
            <ul class="d-flex align-items-center m-0 p-0 list-inline">
              <li v-for="(item, index1) in item.otherInfo" :key="index1">
                <a href="" class="pe-3 text-white d-flex align-items-center">
                  {{ item.value }}
                  <i class="material-symbols-outlined md-14 ms-1">
                    {{ item.class }}
                  </i>
                </a>
              </li>
            </ul>
          </div>
        </div>
        <a
          href="#"
          class="image-edit-btn material-symbols-outlined md-16"
          v-b-tooltip.hover.top="'Edit or Remove'"
        >
          drive_file_rename_outline
        </a>
      </div>
    </div>
  </div>

  <FsLightbox
    :toggler="toggler"
    :sources="[
      require('@/assets/images/page-img/51.jpg'),
      require('@/assets/images/page-img/52.jpg'),
      require('@/assets/images/page-img/53.jpg'),
      require('@/assets/images/page-img/54.jpg'),
      require('@/assets/images/page-img/55.jpg'),
      require('@/assets/images/page-img/56.jpg'),
    ]"
  />
</template>
<script>
import FsLightbox from "fslightbox-vue/v3";
// import { socialvue } from '../../../config/pluginInit'
export default {
  name: "ProfileImage",
  mounted() {
    // socialvue.index()
  },
  components: {
    FsLightbox,
  },
  data() {
    return {
      toggler: false,
      profileImages: [
        {
          img: require("../assets/images/page-img/51.jpg"),
          otherInfo: [
            {
              class: "thumb_up",
              value: 10,
            },
            {
              class: "chat_bubble_outline",
              value: 2,
            },
            {
              class: "forward",
              value: 1,
            },
          ],
        },
        {
          img: require("../assets/images/page-img/52.jpg"),
          otherInfo: [
            {
              class: "thumb_up",
              value: 10,
            },
            {
              class: "chat_bubble_outline",
              value: 2,
            },
            {
              class: "forward",
              value: 1,
            },
          ],
        },
        {
          img: require("../assets/images/page-img/53.jpg"),
          otherInfo: [
            {
              class: "thumb_up",
              value: 120,
            },
            {
              class: "chat_bubble_outline",
              value: 21,
            },
            {
              class: "forward",
              value: 10,
            },
          ],
        },
        {
          img: require("../assets/images/page-img/54.jpg"),
          otherInfo: [
            {
              class: "thumb_up",
              value: 100,
            },
            {
              class: "chat_bubble_outline",
              value: 20,
            },
            {
              class: "forward",
              value: 120,
            },
          ],
        },
        {
          img: require("../assets/images/page-img/55.jpg"),
          otherInfo: [
            {
              class: "thumb_up",
              value: 107,
            },
            {
              class: "chat_bubble_outline",
              value: 20,
            },
            {
              class: "forward",
              value: 101,
            },
          ],
        },
        {
          img: require("../assets/images/page-img/56.jpg"),
          otherInfo: [
            {
              class: "thumb_up",
              value: 105,
            },
            {
              class: "chat_bubble_outline",
              value: 25,
            },
            {
              class: "forward",
              value: 15,
            },
          ],
        },
        {
          img: require("../assets/images/page-img/57.jpg"),
          otherInfo: [
            {
              class: "thumb_up",
              value: 107,
            },
            {
              class: "chat_bubble_outline",
              value: 27,
            },
            {
              class: "forward",
              value: 17,
            },
          ],
        },
        {
          img: require("../assets/images/page-img/58.jpg"),
          otherInfo: [
            {
              class: "thumb_up",
              value: 106,
            },
            {
              class: "chat_bubble_outline",
              value: 26,
            },
            {
              class: "forward",
              value: 14,
            },
          ],
        },
        {
          img: require("../assets/images/page-img/59.jpg"),
          otherInfo: [
            {
              class: "thumb_up",
              value: 10,
            },
            {
              class: "chat_bubble_outline",
              value: 24,
            },
            {
              class: "forward",
              value: 14,
            },
          ],
        },
        {
          img: require("../assets/images/page-img/60.jpg"),
          otherInfo: [
            {
              class: "thumb_up",
              value: 10,
            },
            {
              class: "chat_bubble_outline",
              value: 24,
            },
            {
              class: "forward",
              value: 1,
            },
          ],
        },
        {
          img: require("../assets/images/page-img/61.jpg"),
          otherInfo: [
            {
              class: "thumb_up",
              value: 60,
            },
            {
              class: "chat_bubble_outline",
              value: 30,
            },
            {
              class: "forward",
              value: 10,
            },
          ],
        },
        {
          img: require("../assets/images/page-img/62.jpg"),
          otherInfo: [
            {
              class: "thumb_up",
              value: 60,
            },
            {
              class: "chat_bubble_outline",
              value: 24,
            },
            {
              class: "forward",
              value: 10,
            },
          ],
        },
        {
          img: require("../assets/images/page-img/63.jpg"),
          otherInfo: [
            {
              class: "thumb_up",
              value: 60,
            },
            {
              class: "chat_bubble_outline",
              value: 30,
            },
            {
              class: "forward",
              value: 10,
            },
          ],
        },
        {
          img: require("../assets/images/page-img/64.jpg"),
          otherInfo: [
            {
              class: "thumb_up",
              value: 60,
            },
            {
              class: "chat_bubble_outline",
              value: 30,
            },
            {
              class: "forward",
              value: 10,
            },
          ],
        },
        {
          img: require("../assets/images/page-img/65.jpg"),
          otherInfo: [
            {
              class: "thumb_up",
              value: 60,
            },
            {
              class: "chat_bubble_outline",
              value: 30,
            },
            {
              class: "forward",
              value: 10,
            },
          ],
        },
        {
          img: require("../assets/images/page-img/51.jpg"),
          otherInfo: [
            {
              class: "thumb_up",
              value: 10,
            },
            {
              class: "chat_bubble_outline",
              value: 2,
            },
            {
              class: "forward",
              value: 1,
            },
          ],
        },
        {
          img: require("../assets/images/page-img/52.jpg"),
          otherInfo: [
            {
              class: "thumb_up",
              value: 10,
            },
            {
              class: "chat_bubble_outline",
              value: 2,
            },
            {
              class: "forward",
              value: 1,
            },
          ],
        },
        {
          img: require("../assets/images/page-img/53.jpg"),
          otherInfo: [
            {
              class: "thumb_up",
              value: 120,
            },
            {
              class: "chat_bubble_outline",
              value: 21,
            },
            {
              class: "forward",
              value: 10,
            },
          ],
        },
        {
          img: require("../assets/images/page-img/54.jpg"),
          otherInfo: [
            {
              class: "thumb_up",
              value: 100,
            },
            {
              class: "chat_bubble_outline",
              value: 20,
            },
            {
              class: "forward",
              value: 120,
            },
          ],
        },
        {
          img: require("../assets/images/page-img/55.jpg"),
          otherInfo: [
            {
              class: "thumb_up",
              value: 107,
            },
            {
              class: "chat_bubble_outline",
              value: 20,
            },
            {
              class: "forward",
              value: 101,
            },
          ],
        },
        {
          img: require("../assets/images/page-img/56.jpg"),
          otherInfo: [
            {
              class: "thumb_up",
              value: 105,
            },
            {
              class: "chat_bubble_outline",
              value: 25,
            },
            {
              class: "forward",
              value: 15,
            },
          ],
        },
        {
          img: require("../assets/images/page-img/57.jpg"),
          otherInfo: [
            {
              class: "thumb_up",
              value: 107,
            },
            {
              class: "chat_bubble_outline",
              value: 27,
            },
            {
              class: "forward",
              value: 17,
            },
          ],
        },
        {
          img: require("../assets/images/page-img/58.jpg"),
          otherInfo: [
            {
              class: "thumb_up",
              value: 106,
            },
            {
              class: "chat_bubble_outline",
              value: 26,
            },
            {
              class: "forward",
              value: 14,
            },
          ],
        },
        {
          img: require("../assets/images/page-img/59.jpg"),
          otherInfo: [
            {
              class: "thumb_up",
              value: 10,
            },
            {
              class: "chat_bubble_outline",
              value: 24,
            },
            {
              class: "forward",
              value: 14,
            },
          ],
        },
      ],
    };
  },
};
</script>
