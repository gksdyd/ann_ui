<template>
  <div class="content-inner">
    <b-container>
      <b-row>
        <b-col sm="12">
          <iq-card>
            <template v-slot:headerTitle>
              <h4 class="card-title">Fontawesome Icon</h4>
            </template>
            <b-card-body class="pt-0">
              <p>
                Use Class
                <code>&#60;i class="far fa-address-book"&#62;&#60;/i&#62;</code>
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
                    <i :class="icon.class" aria-hidden="true"></i
                    >{{ icon.name }}
                  </a>
                </b-col>
              </b-row>
              <div class="col-sm-12 text-center mt-3">
                <a
                  href="https://fontawesome.com/v4.7.0/"
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
  { name: "address-book", class: "far fa-address-book" },
  { name: "envelope-open", class: "fa fa-envelope-open" },
  { name: "id-card", class: "fa fa-id-card" },
  { name: "telegram", class: "fab fa-telegram" },
  { name: "user-circle", class: "fa fa-user-circle" },
  { name: "icard", class: "far fa-address-card" },
  { name: "asterisk", class: "fa fa-asterisk" },
  { name: "car", class: "fa fa-car" },
  { name: "bars", class: "fa fa-bars" },
  { name: "battery-full", class: "fa fa-battery-full" },
  { name: "bluetooth", class: "fab fa-bluetooth-b" },
  { name: "book", class: "fa fa-book" },
  { name: "bug", class: "fa fa-bug" },
  { name: "building", class: "fa fa-building" },
  { name: "calculator", class: "fa fa-calculator" },
  { name: "calendar", class: "fa fa-calendar" },
  { name: "camera", class: "fa fa-camera" },
  { name: "comment", class: "far fa-comments" },
  { name: "crop", class: "fa fa-crop" },
  { name: "download", class: "fa fa-download" },
  { name: "folder", class: "fa fa-folder" },
  { name: "gift", class: "fa fa-gift" },
  { name: "users", class: "fa fa-users" },
  { name: "hashtag", class: "fa fa-hashtag" },
  { name: "home", class: "fa fa-home" },
  { name: "lock", class: "fa fa-lock" },
  { name: "graduation-cap", class: "fa fa-graduation-cap" },
  { name: "paper-plane", class: "fa fa-paper-plane" },
  { name: "star", class: "fa fa-star" },
  { name: "tag", class: "fa fa-tag" },
  { name: "trash", class: "fa fa-trash" },
  { name: "upload", class: "fa fa-upload" },
  { name: "university", class: "fa fa-university" },
  { name: "wifi", class: "fa fa-wifi" },
  { name: "thumbs-up", class: "fa fa-thumbs-up" },
  { name: "train", class: "fa fa-train" },
  { name: "file", class: "fa fa-file" },
  { name: "snapchat", class: "fab fa-snapchat" },
  { name: "twitter", class: "fab fa-twitter" },
  { name: "wordpress", class: "fab fa-wordpress" },
  { name: "html", class: "fab fa-html5" },
  { name: "css", class: "fab fa-css3-alt" },
];
</script>
