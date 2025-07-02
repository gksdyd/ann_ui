<template>
  <div id="content-page" class="content-inner">
    <div class="container position-relative p-0">
      <div class="header-cover-img"></div>
    </div>
    <b-container>
      <b-row>
        <b-col sm="12">
          <iq-card class="profile-box">
            <b-card-body>
              <b-row class="align-items-center item-header-content">
                <b-col lg="4" class="profile-left">
                  <ul
                    class="d-flex align-items-center justify-content-center gap-3 list-inline p-0 m-0 mb-3 flex-wrap"
                  >
                    <li class="d-flex align-items-center gap-1">
                      <img
                        src="@/assets/images/gamipress/coin.svg"
                        class="img-fluid avatar-24"
                        alt="coin"
                        loading="lazy"
                      />
                      <h6 class="font-size-14 fw-semibold">
                        {{ coins }} Coins
                      </h6>
                    </li>
                    <li class="d-flex align-items-center gap-1">
                      <img
                        src="@/assets/images/gamipress/credit.svg"
                        class="img-fluid avatar-24"
                        alt="credit"
                        loading="lazy"
                      />
                      <h6 class="font-size-14 fw-semibold">
                        {{ credits }} Credits
                      </h6>
                    </li>
                    <li class="d-flex align-items-center gap-1">
                      <img
                        src="@/assets/images/gamipress/gems.svg"
                        class="img-fluid avatar-24"
                        alt="coin"
                        loading="lazy"
                      />
                      <h6 class="font-size-14 fw-semibold">{{ gems }} Gems</h6>
                    </li>
                  </ul>
                  <div class="social-links">
                    <ul
                      class="social-data-block d-flex align-items-center justify-content-center list-inline p-0 m-0"
                    >
                      <li class="text-center pe-3">
                        <a href="#">
                          <img
                            src="@/assets/images/icon/08.png"
                            class="img-fluid rounded"
                            alt="facebook"
                            loading="lazy"
                          />
                        </a>
                      </li>
                      <li class="text-center pe-3">
                        <a href="#">
                          <img
                            src="@/assets/images/icon/09.png"
                            class="img-fluid rounded"
                            alt="Twitter"
                            loading="lazy"
                          />
                        </a>
                      </li>
                      <li class="text-center pe-3">
                        <a href="#">
                          <img
                            src="@/assets/images/icon/10.png"
                            class="img-fluid rounded"
                            alt="Instagram"
                            loading="lazy"
                          />
                        </a>
                      </li>
                      <li class="text-center pe-3">
                        <a href="#">
                          <img
                            src="@/assets/images/icon/11.png"
                            class="img-fluid rounded"
                            alt="Google plus"
                            loading="lazy"
                          />
                        </a>
                      </li>
                      <li class="text-center pe-3">
                        <a href="#">
                          <img
                            src="@/assets/images/icon/12.png"
                            class="img-fluid rounded"
                            alt="You tube"
                            loading="lazy"
                          />
                        </a>
                      </li>
                      <li class="text-center md-pe-3 pe-0">
                        <a href="#">
                          <img
                            src="@/assets/images/icon/13.png"
                            class="img-fluid rounded"
                            alt="linkedin"
                            loading="lazy"
                          />
                        </a>
                      </li>
                      <!-- Add other social media links similarly -->
                    </ul>
                  </div>
                </b-col>
                <b-col lg="4" class="text-center profile-center">
                  <div class="header-avatar position-relative d-inline-block">
                    <span class="change-profile-image bg-primary rounded-pill">
                      <span
                        class="material-symbols-outlined text-white font-size-16"
                        >photo_camera</span
                      >
                    </span>
                    <img
                      src="@/assets/images/user/1.jpg"
                      alt="user"
                      class="avatar-150 border border-4 border-white rounded-3"
                    />
                    <span
                      class="badge bg-success fw-500 letter-spacing-1 chat-status"
                      >online</span
                    >
                  </div>
                  <h5
                    class="d-flex align-items-center justify-content-center gap-1 mb-2"
                  >
                    {{ username }}
                    <span
                      class="badge bg-primary rounded-pill material-symbols-outlined font-size-14 p-0 custom-done"
                      >done</span
                    >
                  </h5>
                  <ul
                    class="d-flex align-items-center justify-content-center gap-3 list-inline p-0 m-0"
                  >
                    <li class="d-flex align-items-center gap-1">
                      <h6 class="material-symbols-outlined font-size-14">
                        location_on
                      </h6>
                      <span class="font-size-14 text-uppercase fw-500">{{
                        location
                      }}</span>
                    </li>
                    <li class="d-flex align-items-center gap-1">
                      <h6 class="material-symbols-outlined font-size-14">
                        globe_asia
                      </h6>
                      <a
                        href="https://smartinvestmentoff.com/"
                        class="font-size-14 fw-500 text-body"
                        >{{ website }}</a
                      >
                    </li>
                  </ul>
                </b-col>
                <b-col class="profile-right">
                  <ul
                    class="user-meta list-inline p-0 d-flex align-items-center justify-content-center"
                  >
                    <li>
                      <h5>{{ posts }}</h5>
                      Posts
                    </li>
                    <li>
                      <h5>{{ comments }}</h5>
                      Comments
                    </li>
                    <li>
                      <h5>{{ views }}K</h5>
                      Views
                    </li>
                  </ul>
                </b-col>
              </b-row>
            </b-card-body>
          </iq-card>
          <iq-card class="iq-card">
            <div class="iq-card-body p-0">
              <div class="user-tabing item-list-tabs">
                <tab-nav
                  :pills="true"
                  id="pills-tab"
                  class="nav nav-pills d-flex align-items-center justify-content-center profile-feed-items p-0 m-0 rounded"
                >
                  <tab-nav-items
                    widthclass="nav-link active d-flex flex-md-column align-items-center flex-row justify-content-center gap-2"
                    class="col-12 col-sm-3"
                    :active="true"
                    id="pills-feed-tab"
                    href="#profile-feed"
                    ariaControls="pills-home"
                    role="tab"
                    :ariaSelected="true"
                    title="Timeline"
                  >
                    <template #title>
                      <span class="icon rounded-3"
                        ><span class="material-symbols-outlined"
                          >calendar_month</span
                        ></span
                      >
                      <p class="mb-0 mt-0 mt-md-3">Timeline</p>
                    </template>
                  </tab-nav-items>
                  <tab-nav-items
                    class="col-12 col-sm-3"
                    widthclass="nav-link d-flex flex-md-column align-items-center flex-row justify-content-center gap-2"
                    :active="false"
                    id="pills-activity-tab"
                    href="#profile-activity"
                    ariaControls="pills-profile"
                    role="tab"
                    :ariaSelected="false"
                  >
                    <template #title>
                      <span class="icon rounded-3"
                        ><span class="material-symbols-outlined"
                          >person</span
                        ></span
                      >
                      <p class="mb-0 mt-0 mt-md-3">About</p>
                    </template>
                  </tab-nav-items>
                  <tab-nav-items
                    class="col-12 col-sm-3"
                    widthclass="nav-link d-flex flex-md-column align-items-center flex-row justify-content-center gap-2"
                    :active="false"
                    id="pills-friend-tab"
                    href="#profile-friends"
                    ariaControls="pills-contact"
                    role="tab"
                    :ariaSelected="false"
                  >
                    <template #title>
                      <span class="icon rounded-3"
                        ><span class="material-symbols-outlined"
                          >group</span
                        ></span
                      >
                      <p class="mb-0 mt-0 mt-md-3">Friends</p>
                    </template>
                  </tab-nav-items>
                  <tab-nav-items
                    class="col-12 col-sm-3"
                    widthclass="nav-link d-flex flex-md-column align-items-center flex-row justify-content-center gap-2"
                    :active="false"
                    id="pills-profile-tab"
                    href="#profile-profile"
                    ariaControls="pills-contact"
                    role="tab"
                    :ariaSelected="false"
                  >
                    <template #title>
                      <span class="icon rounded-3"
                        ><span class="material-symbols-outlined"
                          >image</span
                        ></span
                      >
                      <p class="mb-0 mt-0 mt-md-3">Photos</p>
                    </template>
                  </tab-nav-items>
                </tab-nav>
              </div>
            </div>
          </iq-card>
        </b-col>
        <b-col class="col-sm-12">
          <div class="tab-content">
            <tab-content-item
              :active="true"
              id="profile-feed"
              aria-labelled-by="pills-feed-tab"
            >
              <div class="iq-card-body p-0">
                <b-row>
                  <b-col lg="4">
                    <iq-card>
                      <template v-slot:body>
                        <a href="#" class="d-inline-flex align-items-center"
                          ><span
                            class="badge badge-pill bg-primary font-weight-normal me-1 material-symbols-outlined md-14"
                            style="font-size: 24px; line-height: 1"
                            >grade</span
                          ><span>27 Items for you</span></a
                        >
                      </template>
                    </iq-card>
                    <iq-card headerClass="border-bottom">
                      <template v-slot:headerTitle>
                        <h4 class="card-title">Life Event</h4>
                      </template>
                      <template v-slot:headerAction>
                        <p class="m-0"><a href="#"> Create </a></p>
                      </template>
                      <template v-slot:body>
                        <div class="row">
                          <div
                            class="col-sm-12"
                            v-for="(event, index) in lifeEvent"
                            :key="index"
                          >
                            <div class="event-post position-relative">
                              <a href="#">
                                <img
                                  :src="event.img"
                                  alt="gallary-image"
                                  class="img-fluid rounded"
                              /></a>
                              <div class="job-icon-position">
                                <div
                                  class="job-icon bg-primary p-2 d-inline-block rounded-circle material-symbols-outlined text-white"
                                >
                                  local_mall
                                </div>
                              </div>
                              <div class="iq-card-body text-center p-2">
                                <h5>{{ event.heading }}</h5>
                                <p :class="event.class">{{ event.date }}</p>
                              </div>
                            </div>
                          </div>
                        </div>
                      </template>
                    </iq-card>
                    <div class="fixed-suggestion mb-4">
                      <iq-card headerClass="border-bottom">
                        <template v-slot:headerTitle>
                          <h4 class="card-title">Photos</h4>
                        </template>
                        <template v-slot:headerAction>
                          <p class="m-0"><a href="#">Add Photo </a></p>
                        </template>
                        <template v-slot:body>
                          <ul class="profile-img-gallary p-0 m-0 list-unstyled">
                            <li
                              v-for="(item, index) in photos"
                              :key="index"
                              @click="($event) => (toggler = !toggler)"
                            >
                              <a data-fslightbox="gallery">
                                <img
                                  :src="item.image"
                                  alt="Responsive image"
                                  class="img-fluid"
                                  loading="lazy"
                                />
                              </a>
                            </li>
                          </ul>
                        </template>
                      </iq-card>
                      <iq-card header-class="border-bottom">
                        <template v-slot:headerTitle>
                          <h4 class="card-title">Friends</h4>
                        </template>
                        <template v-slot:headerAction>
                          <p class="m-0">
                            <a href="javacsript:void();">Add New </a>
                          </p>
                        </template>
                        <template v-slot:body>
                          <div
                            class="row row-cols-xl-3 row-cols-md-2 row-cols-2"
                          >
                            <div
                              class="col mt-2 text-center"
                              v-for="(friend, index) in friends"
                              :key="index"
                            >
                              <a href="#">
                                <img
                                  :src="friend.img"
                                  alt="gallary-image"
                                  class="img-fluid"
                              /></a>
                              <h6 class="mt-2 text-center">
                                {{ friend.name }}
                              </h6>
                            </div>
                          </div>
                        </template>
                      </iq-card>
                    </div>
                  </b-col>
                  <div class="col-lg-8">
                    <div id="post-modal-data" class="iq-card">
                      <AddSocialPost @addPost="addPost"></AddSocialPost>
                      <!-- <div  v-for="post in socialPosts" :key="post.id"> -->
                      <social-post :post="post"></social-post>
                      <!-- </div> -->
                    </div>
                  </div>
                </b-row>
              </div>
            </tab-content-item>
            <tab-content-item
              :active="false"
              id="profile-activity"
              aria-labelled-by="pills-activity-tab"
            >
              <!-- <iq-card>
                <template v-slot:body> -->
              <About />
              <!-- </template>
              </iq-card> -->
            </tab-content-item>
            <tab-content-item
              :active="false"
              id="profile-friends"
              aria-labelled-by="pills-friend-tab"
            >
              <iq-card>
                <template v-slot:body>
                  <h2>Friends</h2>
                  <FriendTab />
                </template>
              </iq-card>
            </tab-content-item>
            <tab-content-item
              :active="false"
              id="profile-profile"
              aria-labelled-by="pills-profile-tab"
            >
              <iq-card>
                <template v-slot:body>
                  <h2>Photos</h2>
                  <div class="friend-list-tab mt-2">
                    <tab-nav
                      :pills="true"
                      id="pills"
                      class="nav nav-pills d-flex align-items-center justify-content-left list-item-tabs p-0 mb-3"
                    >
                      <tab-nav-items
                        liClass=" "
                        :active="true"
                        id="pills-photo-you-tab"
                        href="#pill-photosofyou"
                        ariaControls="pills-photo-you-tab"
                        role="tab"
                        :ariaSelected="true"
                        title="Photos of You"
                      />
                      <tab-nav-items
                        liClass=" "
                        :active="false"
                        id="pills-your-photo-tab"
                        href="#pill-your-photos"
                        ariaControls="pills-your-photo-tab"
                        role="tab"
                        :ariaSelected="false"
                        title="Your Photos"
                      />
                    </tab-nav>
                    <div class="tab-content">
                      <tab-content-item
                        :active="true"
                        id="pill-photosofyou"
                        aria-labelled-by="pills-photo-you-tab"
                      >
                        <PhotosOfyou />
                      </tab-content-item>
                      <tab-content-item
                        :active="false"
                        id="pill-your-photos"
                        aria-labelled-by="pills-your-photo-tab"
                      >
                        <YourPhotos />
                      </tab-content-item>
                    </div>
                  </div>
                </template>
              </iq-card>
            </tab-content-item>
          </div>
        </b-col>
      </b-row>
    </b-container>
  </div>
  <FsLightbox
    :toggler="toggler"
    :sources="[
      require('@/assets/images/page-img/g1.jpg'),
      require('@/assets/images/page-img/g2.jpg'),
      require('@/assets/images/page-img/g3.jpg'),
      require('@/assets/images/page-img/g4.jpg'),
      require('@/assets/images/page-img/g5.jpg'),
      require('@/assets/images/page-img/g6.jpg'),
      require('@/assets/images/page-img/g7.jpg'),
      require('@/assets/images/page-img/g8.jpg'),
      require('@/assets/images/page-img/g9.jpg'),
    ]"
  />
</template>
<script>
import { socialvue } from "../../../config/pluginInit";
import ProfileImage from "./ProfileImage";
import FsLightbox from "fslightbox-vue/v3";
import FriendTab from "./ProfileFriends/FriendTab";
import About from "./ProfileFriends/About";
import AddSocialPost from "../../Apps/Social/Components/AddSocialPost";
import SocialPost from "../../Apps/Social/Components/SocialPost.vue";
import Post from "../../../Model/Post";
import { Posts } from "../../../FackApi/api/SocialPost";
import PhotosOfyou from "../../../components/PhotosOfyou.vue";
import YourPhotos from "../../../components/YourPhotos.vue";

export default {
  name: "photos",
  mounted() {
    socialvue.index();
    const body = document.querySelector("body");
    body.classList.add("profile-page");
  },
  unmounted() {
    const body = document.querySelector("body");
    body.classList.remove("profile-page");
  },
  components: {
    FriendTab,
    AddSocialPost,
    About,
    SocialPost,
    FsLightbox,
    PhotosOfyou,
    YourPhotos,
  },

  data() {
    return {
      toggler: false,
      post: new Post(),
      socialPosts: Posts,
      coins: 6765,
      credits: 7180,
      gems: 100,
      username: "Marvin McKinney",
      location: "lyON",
      website: "smartinvestmentoff.com",
      posts: 0,
      comments: 0,
      views: 82.6,
      social: [
        require("../../../assets/images/icon/08.png"),
        require("../../../assets/images/icon/09.png"),
        require("../../../assets/images/icon/10.png"),
        require("../../../assets/images/icon/11.png"),
        require("../../../assets/images/icon/12.png"),
        require("../../../assets/images/icon/13.png"),
      ],
      lifeEvent: [
        {
          img: require("../../../assets/images/page-img/07.jpg"),
          heading: "Started New Job at Apple",
          date: "January 24, 2019",
        },
        {
          img: require("../../../assets/images/page-img/06.jpg"),
          heading: "Freelance Photographer",
          date: "January 24, 2019",
          class: "mb-0",
        },
      ],
      friends: [
        {
          img: require("../../../assets/images/user/05.jpg"),
          name: "Anna Rexia",
        },
        {
          img: require("../../../assets/images/user/06.jpg"),
          name: "Tara Zona",
        },
        {
          img: require("../../../assets/images/user/07.jpg"),
          name: "Polly Tech",
        },
        {
          img: require("../../../assets/images/user/08.jpg"),
          name: "Bill Emia",
        },
        {
          img: require("../../../assets/images/user/09.jpg"),
          name: "Moe Fugga",
        },
        {
          img: require("../../../assets/images/user/10.jpg"),
          name: "Hal Appeno ",
        },
        {
          img: require("../../../assets/images/user/07.jpg"),
          name: "Zack Lee",
        },
        {
          img: require("../../../assets/images/user/06.jpg"),
          name: "Terry Aki",
        },
        {
          img: require("../../../assets/images/user/05.jpg"),
          name: "Greta Life",
        },
      ],
      soicalInfo: [
        {
          name: "Post",
          value: 690,
        },
        {
          name: "Followers",
          value: 90,
        },
        {
          name: "Following",
          value: 100,
        },
      ],
      photos: [
        {
          image: require("../../../assets/images/page-img/g1.jpg"),
        },
        {
          image: require("../../../assets/images/page-img/g2.jpg"),
        },
        {
          image: require("../../../assets/images/page-img/g3.jpg"),
        },
        {
          image: require("../../../assets/images/page-img/g4.jpg"),
        },
        {
          image: require("../../../assets/images/page-img/g5.jpg"),
        },
        {
          image: require("../../../assets/images/page-img/g6.jpg"),
        },
        {
          image: require("../../../assets/images/page-img/g7.jpg"),
        },
        {
          image: require("../../../assets/images/page-img/g8.jpg"),
        },
        {
          image: require("../../../assets/images/page-img/g9.jpg"),
        },
      ],
    };
  },
  methods: {
    addPost(post) {
      this.socialPosts.unshift(post);
    },
  },
};
</script>
<style scoped>
.header-cover-img {
  background-image: url("@/assets/images/page-img/profile-bg1.jpg");
  background-size: cover;
  background-repeat: no-repeat;
}
</style>
