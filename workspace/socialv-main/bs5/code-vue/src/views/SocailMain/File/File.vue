<template>
  <div class="content-inner">
    <b-container>
      <b-row>
        <b-col sm="12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Files</h4>
            </template>
            <template v-slot:headerAction>
              <div class="dropdown">
                <span
                  class="dropdown-btoggle material-symbols-outlined"
                  id="dropdownMenuButton5"
                  data-bs-toggle="dropdown"
                  aria-expanded="false"
                >
                  more_horiz
                </span>
                <div
                  class="dropdown-menu dropdown-menu-start"
                  aria-labelledby="dropdownMenuButton5"
                  style="position: absolute !important; inset: 0 auto auto 0 !important; margin: 0 !important; transform: translate(0, 32px) !important;"
                >
                  <a
                    v-for="(actionItem, index) in action"
                    :key="index"
                    class="dropdown-item d-flex align-items-center"
                    href="#"
                  >
                    <span class="material-symbols-outlined me-2 md-18">{{
                      actionItem.icon
                    }}</span
                    >{{ actionItem.title }}
                  </a>
                </div>
              </div>
            </template>
            <template v-slot:body>
              <b-row class="justify-content-between d-flex">
                <b-col sm="12" md="6">
                  <div id="user_list_datatable_info" class="dataTables_filter">
                    <form class="me-3 position-relative">
                      <div class="form-group mb-0">
                        <input
                          v-model="search"
                          type="search"
                          class="form-control"
                          id="exampleInputSearch"
                          placeholder="Search"
                        />
                      </div>
                    </form>
                  </div>
                </b-col>
                <b-col sm="12" md="6">
                  <div class="user-list-files d-flex justify-content-end">
                    <a href="#" class="chat-icon-phone btn btn-primary-subtle"
                      >Print</a
                    >
                    {{ "" }}
                    <a href="#" class="chat-icon-video btn btn-primary-subtle"
                      >Excel</a
                    >
                    {{ "" }}
                    <a href="#" class="chat-icon-delete btn btn-primary-subtle"
                      >Pdf</a
                    >
                  </div>
                </b-col>
              </b-row>
              <div class="table-responsive">
                <table class="files-lists table table-striped mt-4">
                  <thead>
                    <tr>
                      <th scope="col">
                        <div class="text-center">
                          <input type="checkbox" class="form-check-input" />
                        </div>
                      </th>
                      <th scope="col">File Name</th>
                      <th scope="col">File Type</th>
                      <th scope="col">Date</th>
                      <th scope="col">Size</th>
                      <th scope="col">Author</th>
                      <th scope="col">Action</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr v-for="(item, index) in fileData" :key="index">
                      <td>
                        <div class="text-center">
                          <input type="checkbox" class="form-check-input" />
                        </div>
                      </td>
                      <td>
                        <img
                          class="rounded-circle img-fluid avatar-40 me-2"
                          :src="item.img"
                          alt="profile"
                        />{{ " " }}{{ item.imgTitle }}
                      </td>
                      <td>{{ item.heading }}</td>
                      <td>
                        {{ item.date }}
                      </td>
                      <td>{{ item.size }}</td>
                      <td>
                        {{ item.user }}
                      </td>

                      <td>
                        <div
                          class="flex align-items-center list-user-action lh-1"
                        >
                          <a v-b-tooltip.hover title="Download" href="#"
                            ><i class="material-symbols-outlined">
                              file_download
                            </i></a
                          >
                          {{ "" }}
                          <a v-b-tooltip.hover title="Delete" href="#"
                            ><i class="material-symbols-outlined">
                              delete
                            </i></a
                          >
                        </div>
                      </td>
                    </tr>
                  </tbody>
                </table>
              </div>
            </template>
          </iq-card>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script setup>
import { ref } from "vue";

const search = ref("");
const fileData = ref([
  {
    img: require("../../../assets/images/page-img/43.png"),
    imgTitle: "post report",
    heading: "Document",
    date: "Mar 12, 2020",
    size: "390 kb",
    user: "Anna Sthesia",
  },
  {
    img: require("../../../assets/images/page-img/44.png"),
    imgTitle: "usages",
    heading: "Document",
    date: " Mar 18, 2020 ",
    size: "600 kb",
    user: "Paul Molive",
  },
  {
    img: require("../../../assets/images/page-img/45.png"),
    imgTitle: "Images file",
    heading: "Slide",
    date: "Mar 19, 2020",
    size: "800 kb",
    user: "Bob Frapples",
  },
  {
    img: require("../../../assets/images/page-img/46.png"),
    imgTitle: "total comments ",
    heading: "Document",
    date: "Mar 21, 2020",
    size: "500 kb",
    user: "Barb Ackue",
  },
  {
    img: require("../../../assets/images/page-img/47.png"),
    imgTitle: "popular events",
    heading: "Pdf",
    date: "Mar 24, 2020",
    size: "320 kb",
    user: "Barb Ackue",
  },
  {
    img: require("../../../assets/images/page-img/43.png"),
    imgTitle: "todo list",
    heading: "excel",
    date: "Mar 28, 2020",
    size: "600 kb",
    user: "Ira Membrit",
  },
  {
    img: require("../../../assets/images/page-img/45.png"),
    imgTitle: "music list",
    heading: "pdf",
    date: "Mar 30, 2020",
    size: "900 kb",
    user: "Pete Sariya",
  },
]);

const action = ref([
  {
    icon: "visibility",
    title: "View",
  },
  {
    icon: "delete",
    title: "Delete",
  },
  {
    icon: "edit",
    title: "Edit",
  },
  {
    icon: "print",
    title: "Print",
  },
  {
    icon: "file_download",
    title: "Download",
  },
]);
</script>
<style scoped>
.dropdown-menu {
  position: absolute !important;
  inset: 0 auto auto 0 !important;
  margin: 0 !important;
  transform: translate(0, 33px) !important;
}
.dropdown-menu-right{
  position: absolute !important;
  inset: 0 auto auto 0 !important;
  margin: 0 !important;
  transform: translate(0, 33px) !important;
}
</style>
