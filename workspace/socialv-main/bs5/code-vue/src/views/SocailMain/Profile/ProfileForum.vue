<template>
  <div class="content-inner">
    <div class="container">
      <div class="row">
        <div class="col-sm-12">
          <iq-card>
            <div class="card-body profile-page p-0">
              <div class="profile-header">
                <div class="position-relative">
                  <img
                    src="../../../assets/images/page-img/profile-bg1.jpg"
                    alt="profile-bg"
                    class="rounded img-fluid"
                  />
                  <ul
                    class="header-nav list-inline d-flex flex-wrap justify-end p-0 m-0"
                  >
                    <li>
                      <a href="#" class="material-symbols-outlined"> edit </a>
                    </li>
                    <li>
                      <a href="#" class="material-symbols-outlined">
                        settings
                      </a>
                    </li>
                  </ul>
                </div>
                <div class="user-detail text-center mb-3">
                  <div class="profile-img">
                    <img
                      src="../../../assets/images/user/11.png"
                      alt="profile-img"
                      class="avatar-130 img-fluid"
                    />
                  </div>
                  <div class="profile-detail">
                    <h3 class="">Paul Moliver</h3>
                  </div>
                </div>
                <div
                  class="profile-info py-5 px-md-5 px-3 d-flex align-items-center justify-content-between position-relative"
                >
                  <div class="social-links">
                    <ul
                      class="social-data-block d-flex align-items-center justify-content-between list-inline p-0 m-0"
                    >
                      <li class="text-center pe-3">
                        <a href="#"
                          ><img
                            src="@/assets/images/icon/08.png"
                            class="img-fluid rounded"
                            alt="facebook"
                            loading="lazy"
                        /></a>
                      </li>
                      <li class="text-center pe-3">
                        <a href="#"
                          ><img
                            src="@/assets/images/icon/09.png"
                            class="img-fluid rounded"
                            alt="Twitter"
                            loading="lazy"
                        /></a>
                      </li>
                      <li class="text-center pe-3">
                        <a href="#"
                          ><img
                            src="@/assets/images/icon/10.png"
                            class="img-fluid rounded"
                            alt="Instagram"
                            loading="lazy"
                        /></a>
                      </li>
                      <li class="text-center pe-3">
                        <a href="#"
                          ><img
                            src="@/assets/images/icon/11.png"
                            class="img-fluid rounded"
                            alt="Google plus"
                            loading="lazy"
                        /></a>
                      </li>
                      <li class="text-center pe-3">
                        <a href="#"
                          ><img
                            src="@/assets/images/icon/12.png"
                            class="img-fluid rounded"
                            alt="You tube"
                            loading="lazy"
                        /></a>
                      </li>
                      <li class="text-center pe-0 md-pe-3">
                        <a href="#"
                          ><img
                            src="@/assets/images/icon/13.png"
                            class="img-fluid rounded"
                            alt="linkedin"
                            loading="lazy"
                        /></a>
                      </li>
                    </ul>
                  </div>
                  <div class="social-info">
                    <ul
                      class="social-data-block social-user-meta-list d-flex align-items-center justify-content-center list-inline p-0 m-0 gap-1"
                    >
                      <li class="text-center">
                        <p class="mb-0">690</p>
                        <h6 class="mb-0">Posts</h6>
                      </li>
                      <li class="text-center">
                        <p class="mb-0">206</p>
                        <h6 class="mb-0">Followers</h6>
                      </li>
                      <li class="text-center">
                        <p class="mb-0">100</p>
                        <h6 class="mb-0">Following</h6>
                      </li>
                    </ul>
                  </div>
                </div>
              </div>
            </div>
          </iq-card>
        </div>
        <div class="col-lg-12">
          <!-- <div class="tab-content forum-content"> -->
          <!-- <div class="tab-pane fade active show" id="topicstart" role="tabpanel"> -->

          <iq-card>
            <div class="card-body p-0">
              <div class="user-tabing p-3">
                <div
                  class="d-flex flex-wrap align-items-center justify-content-between gap-3"
                >
                  <ul
                    class="nav nav-pills d-flex align-items-center text-center profile-forum-items p-0 m-0 w-75"
                  >
                    <li
                      v-for="(tab, index) in tabs"
                      :key="index"
                      class="col-sm-3 p-0"
                    >
                      <a
                        :class="tab.classname"
                        data-bs-toggle="pill"
                        :href="tab.link"
                        >{{ tab.title }}</a
                      >
                    </li>
                  </ul>
                  <button type="submit" class="btn btn-primary">
                    Apply Filter
                  </button>
                </div>
              </div>
            </div>
          </iq-card>
          <!-- </div> -->
          <!-- </div> -->
        </div>
        <div class="col-sm-12">
          <div class="tab-content forum-content">
            <div
              class="tab-pane fade active show"
              id="topicstart"
              role="tabpanel"
            >
              <iq-card body-class="p-0">
                <template v-slot:body>
                  <div class="table-responsive mb-0">
                    <table class="table forum-table mb-0 rounded">
                      <thead class="bg-primary text-white">
                        <tr>
                          <th>Activity</th>
                          <th>Voices</th>
                          <th>Replies</th>
                          <th>Discussion</th>
                        </tr>
                      </thead>
                      <tbody>
                        <tr
                          v-for="(start, index) in started"
                          :key="index"
                          class="mb-4"
                        >
                          <td class="col-lg-4">
                            <div class="d-flex align-items-center">
                              <img
                                class="img-fluid rounded-circle avatar-40"
                                :src="start.src"
                                alt=""
                              />
                              <div class="media-body ms-3">
                                <h6 class="mb-0">
                                  <a href="#">{{ start.name }}</a>
                                </h6>
                                <p class="mb-0">
                                  {{ start.date }},{{ start.dis2 }}
                                </p>
                              </div>
                            </div>
                          </td>
                          <td class="col-lg-2 h6">{{ start.voices }}</td>
                          <td class="col-lg-2 h6">{{ start.replies }}</td>
                          <td class="col-lg-4">
                            <h6>There are many variations of passages.</h6>
                            <p class="mb-0">
                              <span class="text-dark me-2">{{
                                start.name
                              }}</span
                              >{{ start.dis4
                              }}<span class="text-primary">
                                {{ start.dis3 }}</span
                              >
                            </p>
                          </td>
                        </tr>
                      </tbody>
                    </table>
                  </div>
                </template>
              </iq-card>
            </div>
            <div class="tab-pane fade" id="replies" role="tabpanel">
              <iq-card body-class="p-0">
                <template v-slot:body>
                  <div class="table-responsive">
                    <table class="table forum-table mb-0 rounded">
                      <thead class="bg-primary text-white">
                        <tr>
                          <th>Activity</th>
                          <th>Voices</th>
                          <th>Replies</th>
                          <th>Discussion</th>
                        </tr>
                      </thead>
                      <tbody>
                        <tr
                          v-for="(start, index) in replies"
                          :key="index"
                          class="mb-4"
                        >
                          <td class="col-lg-4">
                            <div class="d-flex align-items-center">
                              <img
                                class="img-fluid rounded-circle avatar-40"
                                :src="start.src"
                                alt=""
                              />
                              <div class="media-body ms-3">
                                <h6 class="mb-0">
                                  <a href="#">{{ start.name }}</a>
                                </h6>
                                <p class="mb-0">
                                  {{ start.date }},{{ start.dis2 }}
                                </p>
                              </div>
                            </div>
                          </td>
                          <td class="col-lg-2 h6">{{ start.voices }}</td>
                          <td class="col-lg-2 h6">{{ start.replies }}</td>
                          <td class="col-lg-4">
                            <h6>There are many variations of passages.</h6>
                            <p class="mb-0">
                              <span class="text-dark me-2">{{
                                start.name
                              }}</span
                              >{{ start.dis4
                              }}<span class="text-primary">
                                {{ start.dis3 }}</span
                              >
                            </p>
                          </td>
                        </tr>
                      </tbody>
                    </table>
                  </div>
                </template>
              </iq-card>
            </div>
            <div class="tab-pane fade" id="likedtopic" role="tabpanel">
              <iq-card body-class="p-0">
                <template v-slot:body>
                  <div class="table-responsive">
                    <table class="table forum-table mb-0 rounded">
                      <thead class="bg-primary text-white">
                        <tr>
                          <th>Activity</th>
                          <th>Voices</th>
                          <th>Replies</th>
                          <th>Discussion</th>
                        </tr>
                      </thead>
                      <tbody>
                        <tr
                          v-for="(start, index) in topics"
                          :key="index"
                          class="mb-4"
                        >
                          <td class="col-lg-4">
                            <div class="d-flex align-items-center">
                              <img
                                class="img-fluid rounded-circle avatar-40"
                                :src="start.src"
                                alt=""
                              />
                              <div class="media-body ms-3">
                                <h6 class="mb-0">
                                  <a href="#">{{ start.name }}</a>
                                </h6>
                                <p class="mb-0">
                                  {{ start.date }},{{ start.dis2 }}
                                </p>
                              </div>
                            </div>
                          </td>
                          <td class="col-lg-2 h6">{{ start.voices }}</td>
                          <td class="col-lg-2 h6">{{ start.replies }}</td>
                          <td class="col-lg-4">
                            <h6>There are many variations of passages.</h6>
                            <p class="mb-0">
                              <span class="text-dark me-2">{{
                                start.name
                              }}</span
                              >{{ start.dis4
                              }}<span class="text-primary">
                                {{ start.dis3 }}</span
                              >
                            </p>
                          </td>
                        </tr>
                      </tbody>
                    </table>
                  </div>
                </template>
              </iq-card>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "ProfileForum",
  mounted() {
    // socialvue.index()
  },
  components: {},
  data() {
    return {
      social: [
        require("../../../assets/images/icon/08.png"),
        require("../../../assets/images/icon/09.png"),
        require("../../../assets/images/icon/10.png"),
        require("../../../assets/images/icon/11.png"),
        require("../../../assets/images/icon/12.png"),
        require("../../../assets/images/icon/13.png"),
      ],
      soicalInfo: [
        {
          name: "Posts",
          value: 690,
        },
        {
          name: "Followers",
          value: 206,
        },
        {
          name: "Following",
          value: 100,
        },
      ],
      tabs: [
        {
          classname: "nav-link active",
          link: "#topicstart",
          title: "Topic Started",
        },
        {
          classname: "nav-link",
          link: "#replies",
          title: "My Replies",
        },
        {
          classname: "nav-link ",
          link: "#likedtopic",
          title: "Liked Topics",
        },
      ],
      started: [
        {
          src: require("../../../assets/images/user/01.jpg"),
          name: "Pete Sariya",
          date: "3 hours",
          voices: "12",
          replies: "3",
          dis2: " 22 minutes ago ",
          dis3: "- Comics",
          dis4: "22 minutes ago ",
        },
        {
          src: require("../../../assets/images/user/02.jpg"),
          name: "Anna Mull",
          date: "3 hours",
          voices: "10",
          replies: "8",
          dis2: " 20 minutes ago ",
          dis3: "- Community Hangout",
          dis4: "20 minutes ago ",
        },
        {
          src: require("../../../assets/images/user/03.jpg"),
          name: "Terry Aki",
          date: "3 hours",
          voices: "8",
          replies: "8",
          dis2: " 18 minutes ago ",
          dis3: "- Community",
          dis4: "18 minutes ago ",
        },
        {
          src: require("../../../assets/images/user/04.jpg"),
          name: "Alex John",
          date: "2 hours",
          voices: "7",
          replies: "6",
          dis2: " 16 minutes ago ",
          dis3: "- expenses",
          dis4: "16 minutes ago ",
        },
        {
          src: require("../../../assets/images/user/05.jpg"),
          name: "Rock Lai",
          date: "2 hours",
          voices: "6",
          replies: "4",
          dis2: " 22 minutes ago ",
          dis3: "- Banking",
          dis4: "22 minutes ago ",
        },
        {
          src: require("../../../assets/images/user/06.jpg"),
          name: "Ira Membrit",
          date: "2 hours",
          voices: "5",
          replies: "4",
          dis2: " 21 minutes ago ",
          dis3: "- expenses",
          dis4: "21 minutes ago ",
        },
        {
          src: require("../../../assets/images/user/07.jpg"),
          name: "Bob Frapples",
          date: "2 hours",
          voices: "4",
          replies: "2",
          dis2: " 20 minutes ago ",
          dis3: "- Community Hangout",
          dis4: "20 minutes ago ",
        },
        {
          src: require("../../../assets/images/user/08.jpg"),
          name: "Paul Moliver",
          date: "2 hours",
          voices: "5",
          replies: "3",
          dis2: " 18 minutes ago ",
          dis3: "- Banking",
          dis4: "18 minutes ago ",
        },
        {
          src: require("../../../assets/images/user/09.jpg"),
          name: "Greta Life",
          date: "2 hours",
          voices: "6",
          replies: "4",
          dis2: " 15 minutes ago ",
          dis3: "- Comics",
          dis4: "15 minutes ago ",
        },
        {
          src: require("../../../assets/images/user/05.jpg"),
          name: "Bearded Wonder",
          date: "3 hours",
          voices: "3",
          replies: "2",
          dis2: " 22 minutes ago ",
          dis3: "- Comics",
          dis4: "22 minutes ago ",
        },
      ],
      replies: [
        {
          src: require("../../../assets/images/user/07.jpg"),
          name: "Bob Frapples",
          date: "2 hours",
          voices: "4",
          replies: "2",
          dis2: " 20 minutes ago ",
          dis3: "- Community Hangout",
          dis4: "20 minutes ago ",
        },
        {
          src: require("../../../assets/images/user/08.jpg"),
          name: "Paul Moliver",
          date: "2 hours",
          voices: "5",
          replies: "3",
          dis2: " 18 minutes ago ",
          dis3: "- Banking",
          dis4: "18 minutes ago ",
        },
        {
          src: require("../../../assets/images/user/01.jpg"),
          name: "Bearded Wonder",
          date: "3 hours",
          voices: "12",
          replies: "3",
          dis2: " 22 minutes ago ",
          dis3: "- Comics",
          dis4: "22 minutes ago ",
        },
        {
          src: require("../../../assets/images/user/02.jpg"),
          name: "Anna Mull",
          date: "3 hours",
          voices: "10",
          replies: "8",
          dis2: " 20 minutes ago ",
          dis3: "- Community Hangout",
          dis4: "20 minutes ago ",
        },
        {
          src: require("../../../assets/images/user/03.jpg"),
          name: "Terry Aki",
          date: "3 hours",
          voices: "8",
          replies: "8",
          dis2: " 22 minutes ago ",
          dis3: "- Community",
          dis4: "22 minutes ago ",
        },
        {
          src: require("../../../assets/images/user/04.jpg"),
          name: "Alex John",
          date: "3 hours",
          voices: "7",
          replies: "6",
          dis2: " 22 minutes ago ",
          dis3: "- expenses",
          dis4: "22 minutes ago ",
        },
        {
          src: require("../../../assets/images/user/05.jpg"),
          name: "Rock Lai",
          date: "3 hours",
          voices: "6",
          replies: "4",
          dis2: " 22 minutes ago ",
          dis3: "- Banking",
          dis4: "22 minutes ago ",
        },
        {
          src: require("../../../assets/images/user/06.jpg"),
          name: "Ira Membrit",
          date: "3 hours",
          voices: "5",
          replies: "4",
          dis2: " 22 minutes ago ",
          dis3: "- expenses",
          dis4: "22 minutes ago ",
        },
        {
          src: require("../../../assets/images/user/09.jpg"),
          name: "Greta Life",
          date: "3 hours",
          voices: "6",
          replies: "4",
          dis2: " 22 minutes ago ",
          dis3: "- Comics",
          dis4: "22 minutes ago ",
        },
        {
          src: require("../../../assets/images/user/05.jpg"),
          name: "Bearded Wonder",
          date: "3 hours",
          voices: "3",
          replies: "2",
          dis2: " 22 minutes ago ",
          dis3: "- Comics",
          dis4: "22 minutes ago ",
        },
      ],
      topics: [
        {
          src: require("../../../assets/images/user/09.jpg"),
          name: "Greta Life",
          date: "2 hours",
          voices: "6",
          replies: "4",
          dis2: " 15 minutes ago ",
          dis3: "- Comics",
          dis4: "15 minutes ago ",
        },
        {
          src: require("../../../assets/images/user/04.jpg"),
          name: "Alex John",
          date: "2 hours",
          voices: "7",
          replies: "6",
          dis2: " 16 minutes ago ",
          dis3: "-  expenses",
          dis4: "16 minutes ago ",
        },
        {
          src: require("../../../assets/images/user/01.jpg"),
          name: "Bearded Wonder",
          date: "3 hours",
          voices: "12",
          replies: "3",
          dis2: " 22 minutes ago ",
          dis3: "- Comics",
          dis4: "22 minutes ago ",
        },
        {
          src: require("../../../assets/images/user/02.jpg"),
          name: "Anna Mull",
          date: "3 hours",
          voices: "10",
          replies: "8",
          dis2: " 20 minutes ago ",
          dis3: "- Community Hangout",
          dis4: "20 minutes ago ",
        },
        {
          src: require("../../../assets/images/user/03.jpg"),
          name: "Terry Aki",
          date: "3 hours",
          voices: "8",
          replies: "8",
          dis2: " 18 minutes ago ",
          dis3: "- Community",
          dis4: "18 minutes ago ",
        },
        {
          src: require("../../../assets/images/user/04.jpg"),
          name: "Alex John",
          date: "2 hours",
          voices: "7",
          replies: "6",
          dis2: " 16 minutes ago ",
          dis3: "- expenses",
          dis4: "16 minutes ago ",
        },
        {
          src: require("../../../assets/images/user/05.jpg"),
          name: "Rock Lai",
          date: "2 hours",
          voices: "8",
          replies: "8",
          dis2: " 22 minutes ago ",
          dis3: "- Banking",
          dis4: "22 minutes ago ",
        },
        {
          src: require("../../../assets/images/user/06.jpg"),
          name: "Ira Membrit",
          date: "2 hours",
          voices: "5",
          replies: "4",
          dis2: " 21 minutes ago ",
          dis3: "- expenses",
          dis4: "21 minutes ago ",
        },
        {
          src: require("../../../assets/images/user/07.jpg"),
          name: "Bob Frapples",
          date: "2 hours",
          voices: "4",
          replies: "2",
          dis2: " 20 minutes ago ",
          dis3: "- Community Hangout",
          dis4: "20 minutes ago ",
        },
        {
          src: require("../../../assets/images/user/08.jpg"),
          name: "Paul Moliver",
          date: "2 hours",
          voices: "5",
          replies: "3",
          dis2: " 18 minutes ago ",
          dis3: "- Banking",
          dis4: "18 minutes ago ",
        },
        {
          src: require("../../../assets/images/user/09.jpg"),
          name: "Greta Life",
          date: "2 hours",
          voices: "6",
          replies: "4",
          dis2: " 15 minutes ago ",
          dis3: "- Comics",
          dis4: "15 minutes ago ",
        },
        {
          src: require("../../../assets/images/user/05.jpg"),
          name: "Bearded Wonder",
          date: "3 hours",
          voices: "3",
          replies: "2",
          dis2: " 22 minutes ago ",
          dis3: "- Comics",
          dis4: "22 minutes ago ",
        },
      ],
    };
  },
  methods: {},
};
</script>
