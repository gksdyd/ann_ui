<template>
  <div>
    <iq-card
      id="post-modal-data"
      body-class="iq-card iq-card-block iq-card-stretch iq-card-height"
      headerClass="border-bottom"
    >
      <template v-slot:headerTitle>
        <!-- <h4 class="card-title">Create Post</h4> -->
        <h5 class="card-title">Add a Post</h5>
      </template>
      <template v-slot:headerAction>
        <div class="dropdown">
          <div class="lh-1" id="post-option" data-bs-toggle="dropdown">
            <span class="material-symbols-outlined"> more_horiz </span>
          </div>
          <div
            class="dropdown-menu dropdown-menu-right"
            aria-labelledby="post-option"
            style=""
          >
            <a
              class="dropdown-item"
              href="#"
              data-bs-toggle="modal"
              data-bs-target="#modal-center"
              >Check in</a
            >
            <a
              class="dropdown-item"
              href="#"
              data-bs-toggle="modal"
              data-bs-target="#modal-center"
              >Live Video</a
            >
            <a
              class="dropdown-item"
              href="#"
              data-bs-toggle="modal"
              data-bs-target="#modal-center"
              >GIF</a
            >
            <a
              class="dropdown-item"
              href="#"
              data-bs-toggle="modal"
              data-bs-target="#modal-center"
              >Watch Party</a
            >
            <a
              class="dropdown-item"
              href="#"
              data-bs-toggle="modal"
              data-bs-target="#modal-center"
              >Play with Friend</a
            >
          </div>
        </div>
      </template>
      <template v-slot:body>
        <div class="mb-5" data-bs-toggle="modal">
          <form class="post-text w-100" action="#">
            <input
              type="text"
              class="form-control rounded px-0"
              placeholder="Write And Share Your Post With Your Friends..."
              style="border: none"
              data-bs-toggle="modal"
              data-bs-target="#modal-center"
            />
          </form>
        </div>
      </template>
      <div class="card-body bg-primary-subtle rounded-bottom-3">
        <div
          class="d-flex align-items-center justify-content-between flex-wrap gap-3"
        >
          <div class="create-post-data">
            <ul class="list-inline m-0 p-0 d-flex align-items-center gap-4">
              <li>
                <a href="#" class="text-body">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    width="18"
                    height="16"
                    viewBox="0 0 18 16"
                    fill="none"
                  >
                    <path
                      fill-rule="evenodd"
                      clip-rule="evenodd"
                      d="M11.5334 1.3761C12.3751 1.7111 12.6326 2.87776 12.9767 3.25276C13.3209 3.62776 13.8134 3.75526 14.0859 3.75526C15.5342 3.75526 16.7084 4.92943 16.7084 6.37693V11.2061C16.7084 13.1478 15.1334 14.7228 13.1917 14.7228H4.80841C2.86591 14.7228 1.29175 13.1478 1.29175 11.2061V6.37693C1.29175 4.92943 2.46591 3.75526 3.91425 3.75526C4.18591 3.75526 4.67841 3.62776 5.02341 3.25276C5.36758 2.87776 5.62425 1.7111 6.46591 1.3761C7.30841 1.0411 10.6917 1.0411 11.5334 1.3761Z"
                      stroke="currentColor"
                      stroke-width="1.5"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                    />
                    <path
                      d="M13.5794 5.91667H13.5869"
                      stroke="currentColor"
                      stroke-width="2"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                    />
                    <path
                      fill-rule="evenodd"
                      clip-rule="evenodd"
                      d="M11.6489 8.94C11.6489 7.47667 10.4631 6.29083 8.99975 6.29083C7.53642 6.29083 6.35059 7.47667 6.35059 8.94C6.35059 10.4033 7.53642 11.5892 8.99975 11.5892C10.4631 11.5892 11.6489 10.4033 11.6489 8.94Z"
                      stroke="currentColor"
                      stroke-width="1.5"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                    />
                  </svg>
                </a>
              </li>
              <li>
                <a href="#" class="text-body">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    width="18"
                    height="18"
                    viewBox="0 0 18 18"
                    fill="none"
                  >
                    <path
                      fill-rule="evenodd"
                      clip-rule="evenodd"
                      d="M7.23043 11.6718C4.02709 11.6718 1.29126 12.156 1.29126 14.096C1.29126 16.036 4.01043 16.5377 7.23043 16.5377C10.4346 16.5377 13.1696 16.0527 13.1696 14.1135C13.1696 12.1743 10.4513 11.6718 7.23043 11.6718Z"
                      stroke="currentColor"
                      stroke-width="1.5"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                    />
                    <path
                      fill-rule="evenodd"
                      clip-rule="evenodd"
                      d="M7.23042 8.90493C9.33292 8.90493 11.0371 7.20076 11.0371 5.09826C11.0371 2.99576 9.33292 1.2916 7.23042 1.2916C5.12875 1.2916 3.42459 2.99576 3.42459 5.09826C3.41709 7.19326 5.10875 8.89743 7.20459 8.90493H7.23042Z"
                      stroke="currentColor"
                      stroke-width="1.5"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                    />
                    <path
                      d="M15.0031 6.22427V9.56594"
                      stroke="currentColor"
                      stroke-width="1.5"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                    />
                    <path
                      d="M16.7079 7.895H13.2996"
                      stroke="currentColor"
                      stroke-width="1.5"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                    />
                  </svg>
                </a>
              </li>
              <li>
                <a href="#" class="text-body">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    width="14"
                    height="18"
                    viewBox="0 0 14 18"
                    fill="none"
                  >
                    <path
                      fill-rule="evenodd"
                      clip-rule="evenodd"
                      d="M9.08341 7.75041C9.08341 6.59935 8.15072 5.66666 7.0005 5.66666C5.84944 5.66666 4.91675 6.59935 4.91675 7.75041C4.91675 8.90063 5.84944 9.83332 7.0005 9.83332C8.15072 9.83332 9.08341 8.90063 9.08341 7.75041Z"
                      stroke="currentColor"
                      stroke-width="1.5"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                    />
                    <path
                      fill-rule="evenodd"
                      clip-rule="evenodd"
                      d="M6.99959 16.5C6.00086 16.5 0.75 12.2486 0.75 7.80274C0.75 4.3222 3.54758 1.5 6.99959 1.5C10.4516 1.5 13.25 4.3222 13.25 7.80274C13.25 12.2486 7.99832 16.5 6.99959 16.5Z"
                      stroke="currentColor"
                      stroke-width="1.5"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                    />
                  </svg>
                </a>
              </li>
            </ul>
          </div>
          <div>
            <ul class="list-inline m-0 p-0 d-flex align-items-center gap-4">
              <li>
                <a href="#" class="text-body fw-medium"> Discard </a>
              </li>
              <li>
                <button type="button" class="btn btn-primary px-4">Post</button>
              </li>
            </ul>
          </div>
        </div>
      </div>
      <b-modal
        id="modal-center"
        title="Create Post"
        closeVariant="primary"
        centered
        size=""
        hideFooter
        headerCloseVariant="primary"
        headerClass="border-bottom"
      >
        <div class="d-flex align-items-center">
          <div class="user-img">
            <img
              src="@/assets/images/user/1.jpg"
              alt="userimg"
              class="avatar-60 rounded-circle img-fluid"
            />
          </div>
          <form class="post-text ms-3 w-100" action="#">
            <input
              type="text"
              class="form-control rounded"
              placeholder="Write something here..."
              style="border: none"
            />
            <!-- <button type="button" data-bs-dismiss="modal">close</button> -->
          </form>
        </div>
        <hr />
        <ul class="d-flex flex-wrap align-items-center list-inline m-0 p-0">
          <li class="col-md-6 mb-3">
            <div class="bg-primary-subtle rounded p-2 pointer me-3">
              <a
                href="javascript:void(0);"
                class="d-inline-block fw-medium text-body"
              >
                <span
                  class="material-symbols-outlined align-middle font-size-20 me-1"
                >
                  add_a_photo
                </span>
                Photo/Video
              </a>
            </div>
          </li>
          <li class="col-md-6 mb-3">
            <div class="bg-primary-subtle rounded p-2 pointer me-3">
              <a
                href="javascript:void(0);"
                class="d-inline-block fw-medium text-body"
              >
                <span
                  class="material-symbols-outlined align-middle font-size-20 me-1"
                >
                  group
                </span>
                Tag Friend
              </a>
            </div>
          </li>
          <li class="col-md-6 mb-3">
            <div class="bg-primary-subtle rounded p-2 pointer me-3">
              <a
                href="javascript:void(0);"
                class="d-inline-block fw-medium text-body"
              >
                <span
                  class="material-symbols-outlined align-middle font-size-20 me-1"
                >
                  sentiment_satisfied
                </span>
                Feeling/Activity
              </a>
            </div>
          </li>
          <li class="col-md-6 mb-3">
            <div class="bg-primary-subtle rounded p-2 pointer me-3">
              <a
                href="javascript:void(0);"
                class="d-inline-block fw-medium text-body"
              >
                <span
                  class="material-symbols-outlined align-middle font-size-20 me-1"
                >
                  location_on
                </span>
                Check in
              </a>
            </div>
          </li>
          <li class="col-md-6 mb-3">
            <div class="bg-primary-subtle rounded p-2 pointer me-3">
              <a
                href="javascript:void(0);"
                class="d-inline-block fw-medium text-body"
              >
                <span
                  class="material-symbols-outlined align-middle font-size-20 me-1"
                >
                  live_tv
                </span>
                Live Video
              </a>
            </div>
          </li>
          <li class="col-md-6 mb-3">
            <div class="bg-primary-subtle rounded p-2 pointer me-3">
              <a
                href="javascript:void(0);"
                class="d-inline-block fw-medium text-body"
              >
                <span
                  class="material-symbols-outlined align-middle font-size-20 me-1"
                >
                  gif_box
                </span>
                GIF
              </a>
            </div>
          </li>
          <li class="col-md-6 mb-3">
            <div class="bg-primary-subtle rounded p-2 pointer me-3">
              <a
                href="javascript:void(0);"
                class="d-inline-block fw-medium text-body"
              >
                <span
                  class="material-symbols-outlined align-middle font-size-20 me-1"
                >
                  celebration
                </span>
                Watch Party
              </a>
            </div>
          </li>
          <li class="col-md-6 mb-3">
            <div class="bg-primary-subtle rounded p-2 pointer me-3">
              <a
                href="javascript:void(0);"
                class="d-inline-block fw-medium text-body"
              >
                <span
                  class="material-symbols-outlined align-middle font-size-20 me-1"
                >
                  sports_esports
                </span>
                Play with Friends
              </a>
            </div>
          </li>
        </ul>
        <hr />
        <div class="other-option">
          <div class="d-flex align-items-center justify-content-between">
            <div class="d-flex align-items-center">
              <div class="user-img me-3">
                <img
                  src="@/assets/images/user/1.jpg"
                  alt="userimg"
                  class="avatar-60 rounded-circle img-fluid"
                />
              </div>
              <h6>Your Story</h6>
            </div>
            <div class="card-post-toolbar">
              <div class="dropdown">
                <span
                  class="dropdown-toggle"
                  data-bs-toggle="dropdown"
                  aria-haspopup="true"
                  aria-expanded="false"
                  role="button"
                >
                  <span class="btn btn-primary">Friend</span>
                </span>
                <div class="dropdown-menu m-0 p-0">
                  <a class="dropdown-item p-3" href="#">
                    <div class="d-flex align-items-top">
                      <span class="material-symbols-outlined"> save </span>
                      <div class="data ms-2">
                        <h6>Public</h6>
                        <p class="mb-0">Anyone on or off Facebook</p>
                      </div>
                    </div>
                  </a>
                  <a class="dropdown-item p-3" href="#">
                    <div class="d-flex align-items-top">
                      <span class="material-symbols-outlined"> cancel </span>
                      <div class="data ms-2">
                        <h6>Friends</h6>
                        <p class="mb-0">Your Friend on facebook</p>
                      </div>
                    </div>
                  </a>
                  <a class="dropdown-item p-3" href="#">
                    <div class="d-flex align-items-top">
                      <span class="material-symbols-outlined">
                        person_remove
                      </span>
                      <div class="data ms-2">
                        <h6>Friends except</h6>
                        <p class="mb-0">Don't show to some friends</p>
                      </div>
                    </div>
                  </a>
                  <a class="dropdown-item p-3" href="#">
                    <div class="d-flex align-items-top">
                      <span class="material-symbols-outlined">
                        notifications
                      </span>
                      <div class="data ms-2">
                        <h6>Only Me</h6>
                        <p class="mb-0">Only me</p>
                      </div>
                    </div>
                  </a>
                </div>
              </div>
            </div>
          </div>
        </div>
        <button
          class="btn btn-primary d-block w-100 mt-3"
          @click="addNewPost(post)"
        >
          Post
        </button>
      </b-modal>
    </iq-card>
  </div>
</template>
<script>
import Post from "../../../../Model/Post";
export default {
  name: "AddSocialPost",
  data() {
    return {
      post: new Post(),
      tab: [
        {
          icon: require("../../../../assets/images/small/07.png"),
          name: " Photo/Video",
        },
        {
          icon: require("../../../../assets/images/small/08.png"),
          name: " Tag Friend",
        },
        {
          icon: require("../../../../assets/images/small/09.png"),
          name: "Feeling/Activity",
        },
        {
          icon: require("../../../../assets/images/small/10.png"),
          name: "Check in",
        },
        {
          icon: require("../../../../assets/images/small/11.png"),
          name: "Live Video",
        },
        {
          icon: require("../../../../assets/images/small/12.png"),
          name: " Gif",
        },
        {
          icon: require("../../../../assets/images/small/13.png"),
          name: "Watch Party",
        },
        {
          icon: require("../../../../assets/images/small/14.png"),
          name: " Play with Friends",
        },
      ],
    };
  },
  methods: {
    showModal() {
      this.$refs["my-modal"].show();
    },
    hideModal() {
      this.$refs["my-modal"].hide();
    },
    toggleModal() {
      // We pass the ID of the button that we want to return focus to
      // when the modal has hidden
      this.$refs["my-modal"].toggle("#toggle-btn");
    },
    addNewPost(post) {
      this.$emit("addPost", post);
      this.post = new Post();
      this.$bvModal.hide("modal1");
    },
    resetPost() {
      this.post = new Post();
    },
    previewImage: function (event) {
      const files = event.target.files;
      Object.keys(files).forEach((i) => {
        const file = files[i];
        const reader = new FileReader();
        reader.onload = (e) => {
          this.post.images.push(e.target.result);
        };
        reader.readAsDataURL(file);
      });
    },
    // Function to add data-bs-dismiss attribute to .btn-close
    addDataDismiss() {
      var els = document.querySelectorAll(".btn-close");
      for (var i = 0; i < els.length; i++) {
        els[i].setAttribute("data-bs-dismiss", "modal");
      }
    },
  },
  mounted() {
    // Call addDataDismiss when the component is mounted
    this.addDataDismiss();
  },
};
</script>
