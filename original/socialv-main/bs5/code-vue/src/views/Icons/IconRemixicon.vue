<template>
  <div class="content-inner">
    <b-container>
      <b-row>
        <b-col sm="12">
          <iq-card>
            <template v-slot:headerTitle>
              <h4 class="card-title">Remixicon Icon</h4>
            </template>
            <b-card-body class="pt-0">
              <p>
                Use Class <code>&lt;i class="ri-4k-fill"&gt;&lt;/i&gt;</code>
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
                  href="https://remixicon.com/"
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
  { name: "4k Fill", class: "ri-4k-fill" },
  { name: "4k line", class: "ri-4k-line" },
  { name: "Account Fill", class: "ri-account-box-fill" },
  { name: "account-pin-box", class: "ri-account-pin-box-line" },
  { name: "award-line", class: "ri-award-line" },
  { name: "award-fill", class: "ri-award-fill" },
  { name: "bookmark-line", class: "ri-bookmark-line" },
  { name: "bookmark-fill", class: "ri-bookmark-fill" },
  { name: "calculator-line", class: "ri-calculator-line" },
  { name: "calculator-fill", class: "ri-calculator-fill" },
  { name: "calendar-line", class: "ri-calendar-line" },
  { name: "calendar-fill", class: "ri-calendar-fill" },
  { name: "reply-line", class: "ri-reply-line" },
  { name: "reply-fill", class: "ri-reply-fill" },
  { name: "send-plane-line", class: "ri-send-plane-line" },
  { name: "send-plane-fill", class: "ri-send-plane-fill" },
  { name: "computer-line", class: "ri-computer-line" },
  { name: "computer-fill", class: "ri-computer-fill" },
  { name: "cellphone-line", class: "ri-cellphone-line" },
  { name: "cellphone-fill", class: "ri-cellphone-fill" },
  { name: "phone-line", class: "ri-phone-line" },
  { name: "phone-fill", class: "ri-phone-fill" },
  { name: "tablet-line", class: "ri-tablet-line" },
  { name: "tablet-fill", class: "ri-tablet-fill" },
  { name: "device-line", class: "ri-device-line" },
  { name: "device-fill", class: "ri-device-fill" },
  { name: "battery-line", class: "ri-battery-line" },
  { name: "battery-fill", class: "ri-battery-fill" },
  { name: "battery-low-line", class: "ri-battery-low-line" },
  { name: "battery-low-fill", class: "ri-battery-low-fill" },
  { name: "file-line", class: "ri-file-line" },
  { name: "file-fill", class: "ri-file-fill" },
  { name: "book-open-line", class: "ri-book-open-line" },
  { name: "book-open-fill", class: "ri-book-open-fill" },
  { name: "lightbulb-line", class: "ri-lightbulb-line" },
  { name: "lightbulb-fill", class: "ri-lightbulb-fill" },
  { name: "map-pin-line", class: "ri-map-pin-line" },
  { name: "map-pin-fill", class: "ri-map-pin-fill" },
  { name: "drop-line", class: "ri-drop-line" },
  { name: "drop-fill", class: "ri-drop-fill" },
];
</script>
