<template>
  <div id="content-page" class="content-inner">
    <b-container>
      <b-row class="gx-4">
        <b-col lg="8">
          <div id="content">
            <div class="row">
              <b-col lg="12">
                <div class="mb-5">
                  <div id="stories" class="storiesWrapper d-flex gap-3">
                    <!-- <Story /> -->
                  </div>
                </div>
              </b-col>
            </div>
            <b-row>
              <b-col sm="12">
                <AddSocialPost @addPost="addPost"></AddSocialPost>
              </b-col>
            </b-row>
            <b-row class="social-post-container">
              <SocialPost />

              <!-- loader LoadMoreContent -->
              <b-col v-if="loadContent" sm="12" class="text-center">
                <img
                  src="../../../assets/images/page-img/page-load-loader.gif"
                  alt="loader"
                  style="height: 100px"
                />
              </b-col>
              <div v-else>
                <LoadMoreContent />
              </div>
            </b-row>
          </div>
        </b-col>
        <!-- <AddSocialPost /> -->
        <b-col lg="4">
          <iq-card bodyClass="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">active users</h4>
            </template>
            <template v-slot:body>
              <ul class="list-inline m-0 p-0">
                <li class="d-flex align-items-center gap-3 mb-3">
                  <img
                    src="@/assets/images/user/01.jpg"
                    alt="story-img"
                    class="avatar-60 avatar-borderd object-cover avatar-rounded img-fluid d-inline-block"
                  />
                  <div>
                    <h5 class="d-inline-block">Arina Event</h5>
                    <span class="profile-status-online"></span>
                    <small class="text-capitalize d-block">Active</small>
                  </div>
                </li>
                <li class="d-flex align-items-center gap-3 mb-3">
                  <img
                    src="@/assets/images/user/02.jpg"
                    alt="story-img"
                    class="avatar-60 avatar-borderd object-cover avatar-rounded img-fluid d-inline-block"
                  />
                  <div>
                    <h5 class="d-inline-block">Darlene Robertson</h5>
                    <span class="profile-status-online"></span>
                    <small class="text-capitalize d-block">Active</small>
                  </div>
                </li>
                <li class="d-flex align-items-center gap-3 mb-3">
                  <img
                    src="@/assets/images/user/03.jpg"
                    alt="story-img"
                    class="avatar-60 avatar-borderd object-cover avatar-rounded img-fluid d-inline-block"
                  />
                  <div>
                    <h5 class="d-inline-block">Jerome Bell</h5>
                    <span class="profile-status-offline"></span>
                    <small class="text-capitalize d-block">7 hours ago</small>
                  </div>
                </li>
                <li class="d-flex align-items-center gap-3">
                  <img
                    src="@/assets/images/user/05.jpg"
                    alt="story-img"
                    class="avatar-60 avatar-borderd object-cover avatar-rounded img-fluid d-inline-block"
                  />
                  <div>
                    <h5 class="d-inline-block">Arlene McCoy</h5>
                    <span class="profile-status-offline"></span>
                    <small class="text-capitalize d-block">4 days ago</small>
                  </div>
                </li>
              </ul>
            </template>
          </iq-card>
          <div class="fixed-suggestion mb-4">
            <iq-card bodyClass="pt-0">
              <template v-slot:headerTitle>
                <h4 class="card-title">Suggestions for you</h4>
              </template>
              <template v-slot:headerAction>
                <small class="fw-500 text-capitalize">See all</small>
              </template>
              <template v-slot:body>
                <ul class="list-inline m-0 p-0">
                  <li class="mb-3">
                    <div
                      class="d-flex align-items-center gap-2 justify-content-between"
                    >
                      <div class="d-flex align-items-center gap-3">
                        <img
                          src="@/assets/images/user/06.jpg"
                          alt="story-img"
                          class="avatar-60 avatar-borderd object-cover avatar-rounded img-fluid d-inline-block"
                        />
                        <div>
                          <div
                            class="d-flex align-items-center justify-content-between gap-2"
                          >
                            <div>
                              <h5>Annette Black</h5>
                              <small class="text-capitalize"
                                >Followed by dribbble + 2 more</small
                              >
                            </div>
                          </div>
                        </div>
                      </div>
                      <div
                        class="d-flex align-items-center flex-shrink-0 gap-2"
                      >
                        <button class="btn btn-primary-subtle p-1 lh-1">
                          <i class="material-symbols-outlined font-size-14">
                            add
                          </i>
                        </button>
                        <button class="btn btn-danger-subtle p-1 lh-1">
                          <i class="material-symbols-outlined font-size-14">
                            close
                          </i>
                        </button>
                      </div>
                    </div>
                  </li>
                  <li class="mb-3">
                    <div
                      class="d-flex align-items-center gap-2 justify-content-between"
                    >
                      <div class="d-flex align-items-center gap-3">
                        <img
                          src="@/assets/images/user/07.jpg"
                          alt="story-img"
                          class="avatar-60 avatar-borderd object-cover avatar-rounded img-fluid d-inline-block"
                        />
                        <div>
                          <div
                            class="d-flex align-items-center justify-content-between gap-2"
                          >
                            <div>
                              <h5>Christopher Plessis</h5>
                              <small class="text-capitalize"
                                >Followed by dribbble + 2 more</small
                              >
                            </div>
                          </div>
                        </div>
                      </div>
                      <div
                        class="d-flex align-items-center flex-shrink-0 gap-2"
                      >
                        <button class="btn btn-primary-subtle p-1 lh-1">
                          <i class="material-symbols-outlined font-size-14">
                            add
                          </i>
                        </button>
                        <button class="btn btn-danger-subtle p-1 lh-1">
                          <i class="material-symbols-outlined font-size-14">
                            close
                          </i>
                        </button>
                      </div>
                    </div>
                  </li>
                  <li>
                    <div
                      class="d-flex align-items-center gap-2 justify-content-between"
                    >
                      <div class="d-flex align-items-center gap-3">
                        <img
                          src="@/assets/images/user/08.jpg"
                          alt="story-img"
                          class="avatar-60 avatar-borderd object-cover avatar-rounded img-fluid d-inline-block"
                        />
                        <div>
                          <div
                            class="d-flex align-items-center justify-content-between gap-2"
                          >
                            <div>
                              <h5>Ellyse Perry</h5>
                              <small class="text-capitalize"
                                >Followed by dribbble + 2 more</small
                              >
                            </div>
                          </div>
                        </div>
                      </div>
                      <div
                        class="d-flex align-items-center flex-shrink-0 gap-2"
                      >
                        <button class="btn btn-primary-subtle p-1 lh-1">
                          <i class="material-symbols-outlined font-size-14">
                            add
                          </i>
                        </button>
                        <button class="btn btn-danger-subtle p-1 lh-1">
                          <i class="material-symbols-outlined font-size-14">
                            close
                          </i>
                        </button>
                      </div>
                    </div>
                  </li>
                </ul>
              </template>
            </iq-card>
            <iq-card bodyClass="pt-0">
              <template v-slot:headerTitle>
                <h4 class="card-title">Latest Activities</h4>
              </template>
              <template v-slot:body>
                <ul class="list-inline m-0 p-0">
                  <li class="d-flex mb-3 pb-3 border-bottom">
                    <img
                      src="@/assets/images/user/09.jpg"
                      alt="story-img"
                      class="avatar-32 avatar-rounded object-cover img-fluid"
                    />
                    <div class="stories-data ms-3">
                      <h6 class="font-size-14">
                        Esther Howard
                        <span class="fw-normal text-body"
                          >reacted comment in to your</span
                        >
                        <span class="fw-normal"> Post.</span>
                      </h6>
                      <small class="text-capitalize">19 min ago</small>
                    </div>
                  </li>
                  <li class="d-flex mb-3 pb-3 border-bottom">
                    <img
                      src="@/assets/images/user/10.jpg"
                      alt="story-img"
                      class="avatar-32 avatar-rounded object-cover img-fluid"
                    />
                    <div class="stories-data ms-3">
                      <h6 class="font-size-14">
                        Monty Carlo
                        <span class="text-body fw-normal">followed you.</span>
                      </h6>
                      <small class="text-capitalize">7 day ago</small>
                    </div>
                  </li>
                  <li class="d-flex mb-3 pb-3 border-bottom">
                    <img
                      src="@/assets/images/user/13.jpg"
                      alt="story-img"
                      class="avatar-32 avatar-rounded object-cover img-fluid"
                    />
                    <div class="stories-data ms-3">
                      <h6 class="font-size-14">
                        Pete Sariya
                        <span class="text-body fw-normal">voted for </span
                        >combination of colors from your brand palette
                      </h6>
                      <small class="text-capitalize">1 month ago</small>
                    </div>
                  </li>
                  <li class="d-flex">
                    <img
                      src="@/assets/images/user/14.jpg"
                      alt="story-img"
                      class="avatar-32 avatar-rounded object-cover img-fluid"
                    />
                    <div class="stories-data ms-3">
                      <h6 class="font-size-14">
                        Dima Davydov
                        <span class="text-body fw-normal"
                          >replied to your comment</span
                        >
                      </h6>
                      <small class="text-capitalize">1 month ago</small>
                    </div>
                  </li>
                </ul>
              </template>
            </iq-card>
          </div>
        </b-col>
        <!-- status elements -->
      </b-row>
    </b-container>
  </div>
</template>
<script>
import * as Zuck from "zuck.js";
import SocialPost from "./Components/SocialPost";
import { Posts } from "../../../FackApi/api/SocialPost";
import AddSocialPost from "./Components/AddSocialPost";
import LoadMoreContent from "./Components/LoadMoreContent.vue";

import { ref, onBeforeUnmount, onMounted } from "vue";
import $ from "jquery";

export default {
  name: "SocialApp",
  components: { AddSocialPost, SocialPost, LoadMoreContent },

  methods: {
    currentSkin() {
      var header = document.getElementById("header");
      var skin = location.href.split("skin=")[1];

      if (!skin) {
        skin = "Snapgram";
      }

      if (skin.indexOf("#") !== -1) {
        skin = skin.split("#")[0];
      }

      var skins = {
        Snapgram: {
          avatars: true,
          list: false,
          autoFullScreen: false,
          cubeEffect: true,
          paginationArrows: true,
        },

        VemDeZAP: {
          avatars: false,
          list: true,
          autoFullScreen: false,
          cubeEffect: false,
          paginationArrows: true,
        },

        FaceSnap: {
          avatars: true,
          list: false,
          autoFullScreen: true,
          cubeEffect: false,
          paginationArrows: true,
        },

        Snapssenger: {
          avatars: false,
          list: false,
          autoFullScreen: false,
          cubeEffect: false,
          paginationArrows: false,
        },
      };

      var el = document.querySelectorAll("#skin option");
      var total = el.length;
      for (var i = 0; i < total; i++) {
        // @ts-ignore
        var what = skin == el[i].value ? true : false;

        if (what) {
          el[i].setAttribute("selected", "selected");
          // @ts-ignore
          header.innerHTML = skin;
          // @ts-ignore
          header.className = skin;
        } else {
          el[i].removeAttribute("selected");
        }
      }
      // @ts-ignore
      return {
        name: skin,
        // @ts-ignore
        params: skins[skin],
      };
    },
    timestamp() {
      var timeIndex = 0;
      var shifts = [
        35,
        60,
        60 * 3,
        60 * 60 * 2,
        60 * 60 * 25,
        60 * 60 * 24 * 4,
        60 * 60 * 24 * 10,
      ];

      var now = new Date();
      var shift = shifts[timeIndex++] || 0;
      var date = new Date(now - shift * 1000);

      return date.getTime() / 1000;
    },
    addPost(post) {
      this.socialPosts.unshift(post);
    },
    addDataDismiss() {
      var els = document.querySelectorAll(".btn-close");
      for (var i = 0; i < els.length; i++) {
        els[i].setAttribute("data-bs-dismiss", "modal");
      }
    },
  },
  mounted() {
    this.addDataDismiss();
    const currentSkin = this.currentSkin();
    return new Zuck("stories", {
      backNative: true,
      previousTap: true,
      skin: currentSkin["name"],
      autoFullScreen: currentSkin["params"]["autoFullScreen"],
      avatars: currentSkin["params"]["avatars"],
      paginationArrows: currentSkin["params"]["paginationArrows"],
      list: currentSkin["params"]["list"],
      cubeEffect: currentSkin["params"]["cubeEffect"],
      localStorage: true,
      timeZone: true,
      stories: [
        Zuck.buildTimelineItem(
          "yourstory",
          require("@/assets/images/user/1.jpg"),
          "Your Story",
          "",
          this.timestamp(),
          [
            [
              "yourstory-1",
              "photo",
              3,
              "https://raw.githubusercontent.com/ramon82/assets/master/zuck.js/stories/1.jpg",
              "https://raw.githubusercontent.com/ramon82/assets/master/zuck.js/stories/1.jpg",
              "",
              false,
              false,
              this.timestamp(),
            ],
            [
              "yourstory-12",
              "video",
              0,
              "https://raw.githubusercontent.com/ramon82/assets/master/zuck.js/stories/2.mp4",
              "https://raw.githubusercontent.com/ramon82/assets/master/zuck.js/stories/2.jpg",
              "",
              false,
              false,
              this.timestamp(),
            ],
          ],
        ),
        Zuck.buildTimelineItem(
          "bobfrapples",
          require("@/assets/images/user/13.jpg"),
          "Bob Frapples",
          "",
          this.timestamp(),
          [
            [
              "bobfrapples-1",
              "video",
              0,
              "https://raw.githubusercontent.com/ramon82/assets/master/zuck.js/stories/4.mp4",
              "https://raw.githubusercontent.com/ramon82/assets/master/zuck.js/stories/4.jpg",
              "",
              false,
              false,
              this.timestamp(),
            ],
            [
              "bobfrapples-2",
              "photo",
              3,
              "https://raw.githubusercontent.com/ramon82/assets/master/zuck.js/stories/5.jpg",
              "https://raw.githubusercontent.com/ramon82/assets/master/zuck.js/stories/5.jpg",
              "",
              false,
              false,
              this.timestamp(),
            ],
            [
              "bobfrapples-3",
              "photo",
              3,
              "https://raw.githubusercontent.com/ramon82/assets/master/zuck.js/stories/3.png",
              "https://raw.githubusercontent.com/ramon82/assets/master/zuck.js/stories/3.png",
              "https://ramon.codes",
              "Visit my Portfolio",
              false,
              this.timestamp(),
            ],
          ],
        ),
        Zuck.buildTimelineItem(
          "gretalife",
          require("@/assets/images/user/14.jpg"),
          "Greta Life",
          "",
          this.timestamp(),
          [
            [
              "gretalife-1",
              "photo",
              5,
              "https://raw.githubusercontent.com/ramon82/assets/master/zuck.js/stories/6.jpg",
              "https://raw.githubusercontent.com/ramon82/assets/master/zuck.js/stories/6.jpg",
              "",
              false,
              false,
              this.timestamp(),
            ],
            [
              "gretalife-2",
              "photo",
              3,
              "https://raw.githubusercontent.com/ramon82/assets/master/zuck.js/stories/7.jpg",
              "https://raw.githubusercontent.com/ramon82/assets/master/zuck.js/stories/7.jpg",
              "http://ladygaga.com",
              false,
              false,
              this.timestamp(),
            ],
          ],
        ),
        Zuck.buildTimelineItem(
          "petesariya-1",
          require("@/assets/images/user/15.jpg"),
          "Pete Sariya",
          "",
          this.timestamp(),
          [
            [
              "petesariya-1",
              "photo",
              5,
              "https://raw.githubusercontent.com/ramon82/assets/master/zuck.js/stories/8.jpg",
              "https://raw.githubusercontent.com/ramon82/assets/master/zuck.js/stories/8.jpg",
              "",
              false,
              false,
              this.timestamp(),
            ],
          ],
        ),
        Zuck.buildTimelineItem(
          "paigeturner",
          require("@/assets/images/user/16.jpg"),
          "Paige Turner",
          "",
          this.timestamp(),
          [
            [
              "paigeturner-1",
              "photo",
              10,
              "https://raw.githubusercontent.com/ramon82/assets/master/zuck.js/stories/9.jpg",
              "https://raw.githubusercontent.com/ramon82/assets/master/zuck.js/stories/9.jpg",
              "",
              false,
              false,
              this.timestamp(),
            ],
          ],
        ),
        Zuck.buildTimelineItem(
          "marcumshaw",
          require("@/assets/images/user/17.jpg"),
          "Marcum Shaw",
          "",
          this.timestamp(),
          [
            [
              "marcumshaw-1",
              "photo",
              10,
              "https://raw.githubusercontent.com/ramon82/assets/master/zuck.js/stories/9.jpg",
              "https://raw.githubusercontent.com/ramon82/assets/master/zuck.js/stories/9.jpg",
              "",
              false,
              false,
              this.timestamp(),
            ],
          ],
        ),
      ],
    });
  },
  data() {
    return {
      suggestionEvent: [
        {
          img: require("../../../assets/images/page-img/42.png"),
          title: "Iqonic Studio",
          des: "Lorem Ipsum",
          otherImg: require("../../../assets/images/small/img-1.jpg"),
        },
        {
          img: require("../../../assets/images/page-img/42.png"),
          title: "Cakes & Bakes ",
          des: "Lorem Ipsum",
          otherImg: require("../../../assets/images/small/img-2.jpg"),
        },
      ],
      event: [
        {
          img: require("../../../assets/images/page-img/s4.jpg"),
          heading: "Web Workshop",
          time: "1 hour ago",
        },
        {
          img: require("../../../assets/images/page-img/s5.jpg"),
          heading: "Fun Events and Festivals",
          time: "4 hour ago",
        },
      ],
      user: {
        background: require("../../../assets/images/page-img/profile-bg1.jpg"),
        profile: require("../../../assets/images/user/11.png"),
        name: "Nik Jone",
        role: " - Web designer",
        about: "Lorem ipsum dolor sit amet, contur adipiscing elit.",
        email: "nikjone@demoo.com",
        phone: "001 2351 256 12",
        location: "USA",
        careated_date: "07 Jan 2020",
      },
      socialPosts: Posts,
      galary: [
        {
          image: require("../../../assets/images/page-img/g1.jpg"),
          href: "#",
        },
        {
          image: require("../../../assets/images/page-img/g2.jpg"),
          href: "#",
        },
        {
          image: require("../../../assets/images/page-img/g3.jpg"),
          href: "#",
        },
        {
          image: require("../../../assets/images/page-img/g4.jpg"),
          href: "#",
        },
        {
          image: require("../../../assets/images/page-img/g5.jpg"),
          href: "#",
        },
        {
          image: require("../../../assets/images/page-img/g6.jpg"),
          href: "#",
        },
        {
          image: require("../../../assets/images/page-img/g7.jpg"),
          href: "#",
        },
        {
          image: require("../../../assets/images/page-img/g8.jpg"),
          href: "#",
        },
        {
          image: require("../../../assets/images/page-img/g9.jpg"),
          href: "#",
        },
      ],
      action: [
        {
          icon: "ri-eye-fill mr-2",
          title: "View",
        },
        {
          icon: "ri-delete-bin-6-fill mr-2",
          title: "Delete",
        },
        {
          icon: "ri-pencil-fill mr-2",
          title: "Edit",
        },
        {
          icon: "ri-printer-fill mr-2",
          title: "Print",
        },
        {
          icon: "ri-file-download-fill mr-2",
          title: "Download",
        },
      ],
      timelineItems: [
        {
          color: "primary",
          title: "Client Login",
          right: "24 November 2019",
          description:
            "Bonbon macaroon jelly beans gummi bears jelly lollipop apple",
          child: {
            type: "img",
            items: [],
          },
        },
        {
          color: "success",
          title: "Scheduled Maintenance",
          right: "23 November 2019",
          description:
            "Bonbon macaroon jelly beans gummi bears jelly lollipop apple",
          child: {
            type: "img",
            items: [],
          },
        },
        {
          color: "danger",
          title: "Dev Meetup",
          right: "20 November 2019",
          description:
            'Bonbon macaroon jelly <b-link href="">beans gummi</b-link> bears jelly lollipop apple',
          child: {
            type: "img",
            items: [
              require("../../../assets/images/user/user-1.jpg"),
              require("../../../assets/images/user/user-2.jpg"),
              require("../../../assets/images/user/user-3.jpg"),
              require("../../../assets/images/user/user-4.jpg"),
              require("../../../assets/images/user/user-5.jpg"),
              require("../../../assets/images/user/user-6.jpg"),
            ],
          },
        },
        {
          color: "primary",
          title: "Client Call",
          right: "19 November 2019",
          description:
            "Bonbon macaroon jelly beans gummi bears jelly lollipop apple",
          child: {
            type: "img",
            items: [],
          },
        },
        {
          color: "warning",
          title: "Mega Event",
          right: "15 November 2019",
          description:
            "Bonbon macaroon jelly beans gummi bears jelly lollipop apple",
          child: {
            type: "img",
            items: [],
          },
        },
      ],
      friends: [
        {
          name: "Paul Molive",
          role: "Web Designer",
          image: require("../../../assets/images/user/user-1.jpg"),
        },
        {
          name: "Paul Molive",
          role: "trainee",
          image: require("../../../assets/images/user/user-1.jpg"),
        },
      ],
      userBio: [
        { title: "Joined", description: "November 15, 2012" },
        { title: "Lives", description: "United States of America" },
        {
          title: "Email",
          description:
            '<a href="mailto:nikjone@gmail.com"> nikjone@gmail.com</a>',
        },
        {
          title: "Url",
          description:
            '<a href="https://getbootstrap.com/docs/4.0/getting-started/introduction/" target="_blank"> www.bootstrap.com </a>',
        },
        {
          title: "Contact",
          description: '<a href="tel:001 4544 565 456">(001) 4544 565 456</a>',
        },
      ],
      story: [
        {
          title: "Web Design",
          time: "1 hour ago",
          image: require("../../../assets/images/page-img/s2.jpg"),
          class: "mb-4",
          isActive: "active",
        },
        {
          title: "App Design",
          time: "4 hour ago",
          image: require("../../../assets/images/page-img/s3.jpg"),
          class: "mb-4",
          isActive: "",
        },
        {
          title: "Abstract Design",
          time: "9 hour ago",
          image: require("../../../assets/images/page-img/s1.jpg"),
          class: "",
          isActive: "",
        },
      ],
      suggestions: [
        {
          name: "Anna Sthesia",
          mutual_friend: "Today",
          image: require("../../../assets/images/user/01.jpg"),
        },
        {
          name: "Paul Molive",
          mutual_friend: "Tomorrow",
          image: require("../../../assets/images/user/02.jpg"),
        },
      ],
      news: [
        {
          description:
            'there is a meetup in your city on friday at 19:00.<a href="#">see details</a>',
        },
        { description: "20% off coupon on selected items at pharmaprix" },
      ],
      twitterFeed: [
        {
          image: require("../../../assets/images/page-img/42.png"),
          name: "UI/Ux Designer",
          description: "Creativity Design",
        },
        {
          image: require("../../../assets/images/page-img/43.png"),
          name: "Marketing",
          description: "Accounting",
        },
        {
          image: require("../../../assets/images/page-img/44.png"),
          name: "Web Developer",
          description: "uniq Concept",
        },
        {
          image: require("../../../assets/images/page-img/45.png"),
          name: "Latest News",
          description: "Line information",
        },
      ],
      recentPages: [
        {
          image: require("../../../assets/images/page-img/46.png"),
          name: "Food town",
        },
        {
          image: require("../../../assets/images/page-img/47.png"),
          name: "Touro Univercity",
        },
        {
          image: require("../../../assets/images/page-img/48.jpg"),
          name: "Moviehouse & Eatery",
        },
        {
          image: require("../../../assets/images/page-img/48.jpg"),
          name: "Coffee + Crisp",
        },
      ],
    };
  },
  setup() {
    const loadContent = ref(true);

    const handleScroll = () => {
      if (window.innerHeight + window.scrollY >= document.body.offsetHeight) {
        setTimeout(() => {
          loadContent.value = false;
        }, 2000);
      }
    };

    onMounted(() => {
      window.addEventListener("scroll", handleScroll);
    });

    onBeforeUnmount(() => {
      window.removeEventListener("scroll", handleScroll);
    });

    return { loadContent };
  },
  // methods: {
  //   addPost(post) {
  //     this.socialPosts.unshift(post);
  //   },
  // },
};
</script>
