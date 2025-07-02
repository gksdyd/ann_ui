<template>
  <div class="email-app-details" :class="active ? 'show' : ''">
    <b-card no-body>
      <b-card-body class="p-0">
        <div class="iq-email-to-list p-3">
          <div class="d-flex justify-content-between">
            <ul
              class="list-inline d-flex align-items-center justify-content-between m-0 p-0"
            >
              <li class="me-3">
                <a
                  href="javascript: void(0);"
                  class="email-remove material-symbols-outlined"
                  @click="closeDetail(item)"
                >
                  keyboard_backspace
                </a>
              </li>
              <li class="me-2" v-b-tooltip.hover title="Mail">
                <b-link href="#" class="material-symbols-outlined"
                  >drafts</b-link
                >
              </li>
              <li class="me-2" v-b-tooltip.hover title="Info">
                <b-link href="#" class="material-symbols-outlined">info</b-link>
              </li>
              <li class="me-2" v-b-tooltip.hover title="Delete">
                <b-link href="#" class="material-symbols-outlined"
                  >delete</b-link
                >
              </li>
              <li class="me-2" v-b-tooltip.hover title="Unread">
                <b-link href="#" class="material-symbols-outlined"
                  >mark_email_unread</b-link
                >
              </li>
              <li class="me-2" v-b-tooltip.hover title="Transfer">
                <b-link href="#" class="material-symbols-outlined"
                  >drive_file_move</b-link
                >
              </li>
              <li class="me-2" v-b-tooltip.hover title="Bookmark">
                <b-link href="#" class="material-symbols-outlined"
                  >turned_in_not</b-link
                >
              </li>
            </ul>
            <div class="iq-email-search d-flex">
              <ul
                class="list-inline d-flex align-items-center justify-content-between m-0 p-0"
              >
                <li class="me-3">
                  <b-link class="font-size-14" href="#">1 of 505</b-link>
                </li>
                <li class="me-2" v-b-tooltip.hover title="Previous">
                  <b-link href="#" class="material-symbols-outlined"
                    >chevron_left</b-link
                  >
                </li>
                <li class="me-2" v-b-tooltip.hover title="Next">
                  <b-link href="#" class="material-symbols-outlined"
                    >navigate_next</b-link
                  >
                </li>
              </ul>
            </div>
          </div>
        </div>
        <hr class="mt-0" />
        <div class="iq-inbox-subject p-3">
          <h5 class="mb-2">{{ item.subject }}</h5>
          <div class="iq-inbox-subject-info">
            <div class="iq-subject-info">
              <img
                :src="require('@/assets/images/user/user-1.jpg')"
                class="img-fluid rounded-circle avatar-80"
                alt="#"
                loading="lazy"
              />
              <div class="iq-subject-status align-self-center">
                <h6 class="mb-0">
                  SocialV Team
                  <a :href="'mailto:' + item.title" class="text-lowercase">{{
                    item.title
                  }}</a>
                </h6>
                <b-dropdown variant="none px-0 py-0" no-caret>
                  <template #button-content>
                    <a class="dropdown-toggle" href="#"> to Me </a>
                  </template>
                  <b-dropdown-menu
                    aria-labelledby="dropdownMenuButton"
                    class="font-size-12"
                  >
                    <table class="iq-inbox-details">
                      <tbody>
                        <tr>
                          <td>from:</td>
                          <td>Medium Daily Digest</td>
                        </tr>
                        <tr>
                          <td>reply-to:</td>
                          <td>noreply@gmail.com</td>
                        </tr>
                        <tr>
                          <td>to:</td>
                          <td>iqonicdesigns@gmail.com</td>
                        </tr>
                        <tr>
                          <td>date:</td>
                          <td>13 Dec 2019, 08:30</td>
                        </tr>
                        <tr>
                          <td>subject:</td>
                          <td>The Golden Rule</td>
                        </tr>
                        <tr>
                          <td>security:</td>
                          <td>Standard encryption</td>
                        </tr>
                      </tbody>
                    </table>
                  </b-dropdown-menu>
                </b-dropdown>
              </div>
              <span class="float-right align-self-center">
                Jan 15, 2029, 10:20AM</span
              >
            </div>
            <div class="iq-inbox-body mt-5">
              <!-- Render email body content here -->
              <p>Hi {{ item.title }},</p>
              <p>
                It is a long established fact that a reader will be distracted
                by the readable content of a page when looking at its layout.
                The point of using Lorem Ipsum is that it has a more-or-less
                normal distribution of letters, as opposed to using 'Content
                here, content here', making it look like readable English. Many
                desktop publishing packages and web page editors now use Lorem
                Ipsum as their default model text, and a search for 'lorem
                ipsum' will uncover many web sites still in their infancy.
              </p>
              <p>
                Various versions have evolved over the years, sometimes by
                accident, sometimes on purpose (injected humour and the like).
              </p>
              <p class="mt-5 mb-0">
                Regards,<span class="d-inline-block w-100">John Deo</span>
              </p>
            </div>
            <hr />
            <div class="attegement">
              <h6 class="mb-2">ATTACHED FILES:</h6>
              <ul>
                <!-- Render attached files here -->
                <li class="icon icon-attegment d-flex align-items-center">
                  <span class="material-symbols-outlined md-18">
                    insert_drive_file
                  </span>
                  <span class="ms-1">mydoc.doc</span>
                </li>
                <li class="icon icon-attegment d-flex align-items-center">
                  <span class="material-symbols-outlined md-18">
                    insert_drive_file
                  </span>
                  <span class="ms-1">mydoc.pdf</span>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </b-card-body>
    </b-card>
  </div>
</template>

<script>
export default {
  name: "EmailDetail",
  props: {
    item: {
      type: Object,
      default: () => ({
        is_selected: false,
        is_unread: false,
        favorite: true,
        title: "",
        subject: "",
        emailTime: "",
      }),
    },
    active: { type: Boolean, default: false },
  },
  mounted() {},
  methods: {
    closeDetail(item) {
      this.$emit("update", item);
    },
  },
};
</script>
