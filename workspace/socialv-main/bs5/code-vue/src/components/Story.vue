<template>
  <div ref="storyContainer">
    <b-card no-body>
      <b-card-body>
        <ul class="list-inline m-0 p-0">
          <li
            :class="`d-flex ${item.mbclass} align-items-center active`"
            v-for="(item, index) in list"
            :key="index"
          >
            <img
              :src="item.image"
              :class="`rounded-pill avatar-70 p-1 border bg-${item.color}-subtle img-fluid`"
              loading="lazy"
            />
            <div class="ms-3">
              <h5>{{ item.design }}</h5>
              <p class="mb-0">{{ item.time }}</p>
            </div>
          </li>
        </ul>
      </b-card-body>
    </b-card>
  </div>
</template>

<script>
import { ref, watch, onMounted } from "vue";
// import Zuck from "zuck.js";

export default {
  mounted() {
    // const stories = new Zuck("stories", {
    //   skin: "snapgram",
    //   avatars: true,
    //   list: false,
    //   cubeEffect: true,
    //   localStorage: true,
    //   autoFullScreen: false,
    //   backButton: true,
    //   previousTap: true,
    //   previousButton: true,
    //   daySeparators: true,
    //   language: "en",
    //   stories: [
    //     {
    //       id: "story1",
    //       photo: "user.jpg",
    //       name: "John Doe",
    //       link: "",
    //       lastUpdated: 1567290150,
    //       items: [
    //         {
    //           type: "photo",
    //           length: 3,
    //           src: "photo.jpg",
    //         },
    //         {
    //           type: "video",
    //           length: 7,
    //           src: "video.mp4",
    //           preview: "video.jpg",
    //         },
    //       ],
    //     },
    //   ],
    // });
  },
};
</script>
