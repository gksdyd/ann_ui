<template>
  <div class="content-inner">
    <b-container>
      <b-row>
        <b-col sm="12">
          <iq-card>
            <template v-slot:headerTitle>
              <h4 class="card-title">Lineawesome Icon</h4>
            </template>
            <b-card-body class="pt-0">
              <p>
                Use Class <code>&lt;i class="las la-bell"&gt;&lt;/i&gt;</code>
              </p>
              <b-row class="mt-3">
                <b-col
                  v-for="(icon, index) in icons"
                  :key="index"
                  lg="2"
                  md="4"
                  sm="6"
                >
                  <a class="iq-icons-list" href="#">
                    <i :class="icon.class"></i>{{ icon.name }}
                  </a>
                </b-col>
              </b-row>
              <div class="col-sm-12 text-center mt-3">
                <a
                  href="https://icons8.com/line-awesome"
                  target="blank"
                  class="btn btn-primary"
                  >View All Icon</a
                >
              </div>
            </b-card-body>
          </iq-card>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script setup>
const icons = [
  { name: "bell", class: "las la-bell" },
  { name: "phone", class: "las la-phone-volume" },
  { name: "radiation", class: "las la-radiation" },
  { name: "dog", class: "las la-dog" },
  { name: "fish", class: "las la-fish" },
  { name: "la-spider", class: "las la-spider" },
  { name: "angle-down", class: "las la-angle-down" },
  { name: "angle-left", class: "las la-angle-left" },
  { name: "angle-right", class: "las la-angle-right" },
  { name: "angle-up", class: "las la-angle-up" },
  { name: "caret-left", class: "las la-caret-left" },
  { name: "caret-right", class: "las la-caret-right" },
  { name: "download", class: "las la-download" },
  { name: "location-arrow", class: "las la-location-arrow" },
  { name: "share", class: "las la-share" },
  { name: "backward", class: "las la-backward" },
  { name: "play", class: "las la-play" },
  { name: "pause", class: "las la-pause" },
  { name: "sync", class: "las la-sync" },
  { name: "volume-down", class: "las la-volume-down" },
  { name: "volume-mute", class: "las la-volume-mute" },
  { name: "volume-off", class: "las la-volume-off" },
  { name: "volume-up", class: "las la-volume-up" },
  { name: "youtube", class: "lab la-youtube" },
  { name: "car", class: "las la-car" },
  { name: "truck", class: "las la-truck" },
  { name: "tree", class: "las la-tree" },
  { name: "pinterest", class: "lab la-pinterest-p" },
  { name: "java", class: "lab la-java" },
  { name: "city", class: "las la-city" },
  { name: "edit", class: "las la-edit" },
  { name: "copy", class: "las la-copy" },
  { name: "cut", class: "las la-cut" },
  { name: "pen", class: "las la-pen" },
  { name: "tag", class: "las la-tag" },
  { name: "save", class: "las la-save" },
  { name: "tasks", class: "las la-tasks" },
  { name: "comment", class: "las la-comment" },
  { name: "video", class: "las la-video" },
  { name: "smile", class: "las la-smile" },
];
</script>
