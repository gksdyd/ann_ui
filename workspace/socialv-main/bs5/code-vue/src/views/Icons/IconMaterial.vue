<template>
  <div class="content-inner">
    <b-container>
      <b-row>
        <b-col sm="12">
          <b-card no-body>
            <div class="card-header d-flex justify-content-between">
              <div class="header-title">
                <h4 class="card-title">Material Icon</h4>
              </div>
            </div>
            <b-card-body class="pt-0">
              <p>
                Use Class
                <code>&#x3C;span
                  class=&#x22;material-symbols-outlined&#x22;&#x3E;search&#x3C;/span&#x3E;</code>
              </p>
              <b-row class="mt-3">
                <b-col v-for="(icon, index) in iconList" :key="index" sm="6" md="4" lg="2">
                  <a class="iq-icons-list d-flex align-items-center" href="#">
                    <i class="material-symbols-outlined me-1">{{ icon.name }}</i>{{ icon.label }}
                  </a>
                </b-col>
              </b-row>
              <div class="col-sm-12 text-center mt-3">
                <a href="https://fonts.google.com/icons?icon.set=Material+Icons&icon.style=Outlined" target="_blank"
                  class="btn btn-primary">View All Icon</a>
              </div>
            </b-card-body>
          </b-card>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script setup>
const iconList = [
  { name: "search", label: "Search" },
  { name: "home", label: "Home" },
  { name: "settings", label: "Settings" },
  { name: "done", label: "Done" },
  { name: "info", label: "Info" },
  { name: "check_circle", label: "Check Circle" },
  { name: "delete", label: "Delete" },
  { name: "shopping_cart", label: "Shopping Cart" },
  { name: "visibility", label: "Visibility" },
  { name: "logout", label: "Logout" },
  { name: "description", label: "Description" },
  { name: "favorite_border", label: "Favorite Border" },
  { name: "lock", label: "Lock" },
  { name: "schedule", label: "Schedule" },
  { name: "language", label: "Language" },
  { name: "face", label: "Face" },
  { name: "help_outline", label: "Help Outline" },
  { name: "event", label: "Event" },
  { name: "verified", label: "Verified" },
  { name: "thumb_up", label: "Thumb Up" },
  { name: "dashboard", label: "Dashboard" },
  { name: "login", label: "Login" },
  { name: "help", label: "Help" },
  { name: "task_alt", label: "Task Alt" },
  { name: "paid", label: "Paid" },
  { name: "article", label: "Article" },
  { name: "lightbulb", label: "Lightbulb" },
  { name: "open_in_new", label: "Open In New" },
  { name: "history", label: "History" },
  { name: "assignment", label: "Assignment" },
];
</script>
