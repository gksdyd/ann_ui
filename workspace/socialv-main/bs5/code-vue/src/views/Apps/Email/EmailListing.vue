<template>
  <div class="position-relative">
        </div>
  <div class="content-inner">
    <b-container class="position-relative overflow-hidden">
      <b-row>
        <b-col lg="3">
          <iq-card>
            <template v-slot:body>
              <div class="iq-email-list">
                <button
                  class="btn btn-primary btn-lg btn-block mb-3 p-2 w-100 d-flex align-items-center"
                  v-b-modal.compose-email-popup
                >
                  <i class="material-symbols-outlined me-2 writ-icon"> send </i
                  >New Message
                </button>
                <tab-nav
                  :pills="true"
                  vertical
                  id="myTab"
                  class="iq-email-ui"
                  @change="updateTab"
                >
                  <tab-nav-items
                    li-class="nav-link p-0"
                    :active="true"
                    id="mail-inbox-tab"
                    ariaControls="mail-inbox"
                    role="tab"
                    :ariaSelected="true"
                  >
                    <template v-slot:title>
                      <div
                        class="d-flex align-items-center justify-content-between"
                      >
                        <span class="d-flex align-items-center"
                          ><i class="material-symbols-outlined md-18"> mail </i
                          >Inbox</span
                        ><span class="badge bg-primary ms-2">4</span>
                      </div>
                    </template>
                  </tab-nav-items>
                  <tab-nav-items
                    li-class="nav-link p-0"
                    :active="false"
                    id="mail-starred-tab"
                    ariaControls="mail-starred"
                    role="tab"
                    :ariaSelected="true"
                  >
                    <template v-slot:title>
                      <div
                        class="d-flex align-items-center justify-content-between"
                      >
                        <span class="d-flex align-items-center">
                          <i class="material-symbols-outlined md-18">
                            star_border </i
                          >Starred
                        </span>
                      </div>
                    </template>
                  </tab-nav-items>
                  <tab-nav-items
                    li-class="nav-link p-0"
                    :active="false"
                    id="mail-snoozed-tab"
                    ariaControls="mail-snoozed"
                    role="tab"
                    :ariaSelected="true"
                  >
                    <template v-slot:title>
                      <div
                        class="d-flex align-items-center justify-content-between"
                      >
                        <span class="d-flex align-items-center">
                          <i class="material-symbols-outlined md-18">
                            watch_later </i
                          >Snoozed
                        </span>
                      </div>
                    </template>
                  </tab-nav-items>
                  <tab-nav-items
                    li-class="nav-link p-0"
                    :active="false"
                    id="mail-draft-tab"
                    ariaControls="mail-draft"
                    role="tab"
                    :ariaSelected="true"
                  >
                    <template v-slot:title>
                      <div
                        class="d-flex align-items-center justify-content-between"
                      >
                        <span class="d-flex align-items-center">
                          <i class="material-symbols-outlined md-18">
                            article </i
                          >Draft
                        </span>
                      </div>
                    </template>
                  </tab-nav-items>
                  <tab-nav-items
                    li-class="nav-link p-0"
                    :active="false"
                    id="mail-sent-tab"
                    ariaControls="mail-sent"
                    role="tab"
                    :ariaSelected="true"
                  >
                    <template v-slot:title>
                      <div
                        class="d-flex align-items-center justify-content-between"
                      >
                        <span class="d-flex align-items-center">
                          <i class="material-symbols-outlined md-18">
                            forward_to_inbox </i
                          >Sent Mail
                        </span>
                      </div>
                    </template>
                  </tab-nav-items>
                  <tab-nav-items
                    li-class="nav-link p-0"
                    :active="false"
                    id="mail-trash-tab"
                    ariaControls="mail-trash"
                    role="tab"
                    :ariaSelected="true"
                  >
                    <template v-slot:title>
                      <div
                        class="d-flex align-items-center justify-content-between"
                      >
                        <span class="d-flex align-items-center">
                          <i class="material-symbols-outlined md-18">
                            delete_outline </i
                          >Trash
                        </span>
                      </div>
                    </template>
                  </tab-nav-items>
                  <tab-nav-items
                    li-class="nav-link p-0"
                    :active="false"
                    id="mail-important-tab"
                    ariaControls="mail-important"
                    role="tab"
                    :ariaSelected="true"
                  >
                    <template v-slot:title>
                      <div
                        class="d-flex align-items-center justify-content-between"
                      >
                        <span class="d-flex align-items-center">
                          <i class="material-symbols-outlined md-18">
                            turned_in_not </i
                          >Important
                        </span>
                      </div>
                    </template>
                  </tab-nav-items>
                  <tab-nav-items
                    li-class="nav-link p-0"
                    :active="false"
                    id="mail-spam-tab"
                    ariaControls="mail-spam"
                    role="tab"
                    :ariaSelected="true"
                  >
                    <template v-slot:title>
                      <div
                        class="d-flex align-items-center justify-content-between"
                      >
                        <span class="d-flex align-items-center">
                          <i class="material-symbols-outlined md-18">
                            report_gmailerrorred </i
                          >Spam
                        </span>
                      </div>
                    </template>
                  </tab-nav-items>
                </tab-nav>
                <h6 class="mt-4 mb-3">Labels</h6>
                <ul class="iq-email-ui iq-email-label list-inline p-0 m-0">
                  <li>
                    <a href="#" class="d-flex align-items-center">
                      <i class="material-symbols-outlined md-18 text-primary"
                        >trip_origin</i
                      >
                      Personal</a
                    >
                  </li>
                  <li>
                    <a href="#" class="d-flex align-items-center">
                      <i class="material-symbols-outlined md-18 text-warning"
                        >trip_origin</i
                      >Company</a
                    >
                  </li>
                  <li>
                    <a href="#" class="d-flex align-items-center"
                      ><i class="material-symbols-outlined md-18 text-success"
                        >trip_origin</i
                      >Important</a
                    >
                  </li>
                  <li>
                    <a href="#" class="d-flex align-items-center"
                      ><i class="material-symbols-outlined md-18 text-info"
                        >trip_origin</i
                      >Private</a
                    >
                  </li>
                  <li>
                    <a href="#" class="d-flex align-items-center"
                      ><i class="material-symbols-outlined md-18 text-warning"
                        >trip_origin</i
                      >Private</a
                    >
                  </li>
                  <li>
                    <a href="#" class="d-flex align-items-center"
                      ><i class="material-symbols-outlined md-18"
                        >add_circle_outline</i
                      >Add New Labels</a
                    >
                  </li>
                </ul>
                <div class="iq-progress-bar-linear d-inline-block w-100">
                  <h6 class="mt-4 mb-3">Storage</h6>
                  <span class="mt-1 d-inline-block w-100"
                    >7.02 GB (46%) of 15 GB used</span
                  >
                </div>
              </div>
            </template>
          </iq-card>
        </b-col>
        <b-col lg="9" class="mail-box-detail">
          <iq-card>
            <div class="iq-email-to-list p-3">
              <div
                class="iq-email-to-list-detail d-flex justify-content-between gap-3"
              >
                <ul
                  class="list-inline d-flex align-items-center justify-content-between m-0 p-0 flex-shrink-0"
                >
                  <li class="me-1">
                    <div id="navbarDropdown" data-bs-toggle="dropdown">
                      <div class="d-flex align-items-center form-check">
                        <input
                          type="checkbox"
                          class="form-check-input"
                          id="customCheck1"
                        />
                        <label
                          class="form-check-label d-flex align-items-center"
                          for="customCheck1"
                        >
                          <i class="material-symbols-outlined"> expand_more </i>
                        </label>
                      </div>
                    </div>
                    <div class="dropdown-menu" aria-labelledby="navbarDropdown">
                      <a class="dropdown-item" href="#">All</a>
                      <a class="dropdown-item" href="#">None</a>
                      <a class="dropdown-item" href="#">Read</a>
                      <a class="dropdown-item" href="#">Unread</a>
                      <a class="dropdown-item" href="#">Starred</a>
                      <a class="dropdown-item" href="#">Unstarred</a>
                    </div>
                  </li>
                  <li
                    class="me-1"
                    data-bs-toggle="tooltip"
                    data-bs-placement="top"
                    title="Reload"
                  >
                    <a
                      href="#"
                      class="d-flex align-items-center justify-content-center"
                      ><i class="material-symbols-outlined md-16">
                        refresh
                      </i></a
                    >
                  </li>
                  <li
                    class="me-1"
                    data-bs-toggle="tooltip"
                    data-bs-placement="top"
                    title="Archive"
                  >
                    <a
                      href="#"
                      class="d-flex align-items-center justify-content-center"
                      ><i class="material-symbols-outlined md-16">
                        drafts
                      </i></a
                    >
                  </li>
                  <li
                    class="me-1"
                    data-bs-toggle="tooltip"
                    data-bs-placement="top"
                    title="Delete"
                  >
                    <a
                      href="#"
                      class="d-flex align-items-center justify-content-center"
                      ><i class="material-symbols-outlined md-16">
                        delete
                      </i></a
                    >
                  </li>
                  <li
                    class="me-1"
                    data-bs-toggle="tooltip"
                    data-bs-placement="top"
                    title="Inbox"
                  >
                    <a
                      href="#"
                      class="d-flex align-items-center justify-content-center"
                      ><i class="material-symbols-outlined md-16">
                        mark_email_unread
                      </i></a
                    >
                  </li>
                  <li
                    data-bs-toggle="tooltip"
                    data-bs-placement="top"
                    title="Zoom"
                  >
                    <a
                      href="#"
                      class="d-flex align-items-center justify-content-center"
                      ><i class="material-symbols-outlined md-16">
                        zoom_out_map
                      </i></a
                    >
                  </li>
                </ul>
                <div class="iq-email-search d-flex flex-shrink-0">
                  <form class="me-2 position-relative searchbox">
                    <div class="form-group mb-0">
                      <input
                        type="email"
                        class="form-control"
                        id="exampleInputEmail1"
                        aria-describedby="emailHelp"
                        placeholder="Search"
                      />
                      <a class="search-link" href="#">
                        <svg
                          width="16"
                          height="17"
                          viewBox="0 0 16 17"
                          fill="none"
                          xmlns="http://www.w3.org/2000/svg"
                        >
                          <circle
                            cx="7.82491"
                            cy="7.82495"
                            r="6.74142"
                            stroke="currentColor"
                            stroke-width="1.5"
                            stroke-linecap="round"
                            stroke-linejoin="round"
                          ></circle>
                          <path
                            d="M12.5137 12.8638L15.1567 15.5"
                            stroke="currentColor"
                            stroke-width="1.5"
                            stroke-linecap="round"
                            stroke-linejoin="round"
                          ></path>
                        </svg>
                      </a>
                    </div>
                  </form>
                  <ul
                    class="list-inline d-flex align-items-center justify-content-between m-0 p-0"
                  >
                    <li class="me-2">
                      <a class="font-size-14" href="javascript:void(0)">
                        1 - 50 of 505
                      </a>
                    </li>
                    <li
                      class="me-1"
                      data-bs-toggle="tooltip"
                      data-bs-placement="top"
                      title="Previous"
                    >
                      <a href="#" class="material-symbols-outlined">
                        keyboard_arrow_left
                      </a>
                    </li>
                    <li
                      class="me-1"
                      data-bs-toggle="tooltip"
                      data-bs-placement="top"
                      title="Next"
                    >
                      <a href="#" class="material-symbols-outlined">
                        keyboard_arrow_right
                      </a>
                    </li>
                    <li
                      class="me-0"
                      data-bs-toggle="tooltip"
                      data-bs-placement="top"
                      title="Setting"
                    >
                      <a href="#" class="material-symbols-outlined">
                        settings
                      </a>
                    </li>
                  </ul>
                </div>
              </div>
            </div>
            <div class="iq-email-listbox">
              <tab-content>
                <EmailDetail
                  :active="active"
                  :item="item"
                  @update="closeDetail"
                />
                <tab-content-item
                  :active="true"
                  id="mail-inbox"
                  aria-labelled-by="mail-inbox-tab"
                  role="tabpanel"
                >
                  <ul class="iq-email-sender-list">
                    <li
                      v-for="(items, index) in inboxItems"
                      :key="index"
                      :class="items.is_unread ? 'iq-unread' : ''"
                    >
                      <EmailItem :items="items" @update="openDetail" />
                    </li>
                  </ul>
                </tab-content-item>
                <tab-content-item
                  :active="false"
                  id="mail-starred"
                  aria-labelled-by="mail-starred-tab"
                  role="tabpanel"
                >
                  <ul class="iq-email-sender-list">
                    <li
                      v-for="(items, index) in starredItems"
                      :key="index"
                      :class="items.is_unread ? 'iq-unread' : ''"
                    >
                      <EmailItem :items="items" @update="openDetail" />
                    </li>
                  </ul>
                </tab-content-item>
                <tab-content-item
                  :active="false"
                  id="mail-snoozed"
                  aria-labelled-by="mail-snoozed-tab"
                  role="tabpanel"
                >
                  <ul class="iq-email-sender-list">
                    <li
                      v-for="(items, index) in snoozedItems"
                      :key="index"
                      :class="items.is_unread ? 'iq-unread' : ''"
                    >
                      <EmailItem :items="items" @update="openDetail" />
                    </li>
                  </ul>
                </tab-content-item>
                <tab-content-item
                  :active="false"
                  id="mail-draft"
                  aria-labelled-by="mail-draft-tab"
                  role="tabpanel"
                >
                  <ul class="iq-email-sender-list">
                    <li
                      v-for="(items, index) in draftItems"
                      :key="index"
                      :class="items.is_unread ? 'iq-unread' : ''"
                    >
                      <EmailItem :items="items" @update="openDetail" />
                    </li>
                  </ul>
                </tab-content-item>
                <tab-content-item
                  :active="false"
                  id="mail-sent"
                  aria-labelled-by="mail-sent-tab"
                  role="tabpanel"
                >
                  <ul class="iq-email-sender-list">
                    <li
                      v-for="(items, index) in sendItems"
                      :key="index"
                      :class="items.is_unread ? 'iq-unread' : ''"
                    >
                      <EmailItem :items="items" @update="openDetail" />
                    </li>
                  </ul>
                </tab-content-item>
                <tab-content-item
                  :active="false"
                  id="mail-trash"
                  aria-labelled-by="mail-trash-tab"
                  role="tabpanel"
                >
                  <ul class="iq-email-sender-list">
                    <li
                      v-for="(items, index) in trashItems"
                      :key="index"
                      :class="items.is_unread ? 'iq-unread' : ''"
                    >
                      <EmailItem :items="items" @update="openDetail" />
                    </li>
                    ``
                  </ul>
                </tab-content-item>
                <tab-content-item
                  :active="false"
                  id="mail-important"
                  aria-labelled-by="mail-important-tab"
                  role="tabpanel"
                >
                  <ul class="iq-email-sender-list">
                    <li
                      v-for="(items, index) in importantItems"
                      :key="index"
                      :class="items.is_unread ? 'iq-unread' : ''"
                    >
                      <EmailItem :items="items" @update="openDetail" />
                    </li>
                  </ul>
                </tab-content-item>
                <tab-content-item
                  :active="false"
                  id="mail-spam"
                  aria-labelled-by="mail-spam-tab"
                  role="tabpanel"
                >
                  <ul class="iq-email-sender-list">
                    <li
                      v-for="(items, index) in spamItems"
                      :key="index"
                      :class="items.is_unread ? 'iq-unread' : ''"
                    >
                      <EmailItem :items="items" @update="openDetail" />
                    </li>
                  </ul>
                </tab-content-item>
              </tab-content>
            </div>
          </iq-card>
        </b-col>
      </b-row>
    </b-container>
  </div>
  <EmailModal/>
</template>
<script>
import { socialvue } from "../../../config/pluginInit";
import {
  inboxEmailData,
  draftEmailsData,
  sendEmailData,
  spamEmailsData,
  starredEmailsData,
  snoozedEmailsData,
  trashEmailsData,
  deletedEmailsData,
  impEmailsData,
} from "../../../FackApi/api/email";
import EmailDetail from "./EmailDetail";
import EmailItem from "./EmailItem";
import EmailModal from './EmailModal'
export default {
  name: "EmailListing",
  components: { EmailItem, EmailDetail, EmailModal },
  mounted() {
    socialvue.index();
  },
  data() {
    return {
      show: false,
      inboxItems: inboxEmailData,
      starredItems: starredEmailsData,
      snoozedItems: snoozedEmailsData,
      draftItems: draftEmailsData,
      sendItems: sendEmailData,
      spamItems: spamEmailsData,
      deleteItems: deletedEmailsData,
      trashItems: trashEmailsData,
      importantItems: impEmailsData,
      active: false,
      dataItem: {
        is_selected: false,
        is_unread: false,
        favorite: true,
        title: "",
        subject: "",
        emailTime: "",
      },
    };
  },
  computed: {
    item() {
      return this.dataItem;
    },
  },
  methods: {
    openDetail(items) {
      this.active = true;
      this.dataItem = items;
    },
    closeDetail(items) {
      this.active = false;
    },
    updateTab(event) {
      this.active = false;
    },
    closeModal(value) {
      this.show = false;
    },
  },
};
</script>

