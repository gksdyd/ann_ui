<template>
  <div class="content-inner">
    <div class="container">
      <div class="row">
        <div class="col-sm-12">
          <h4 class="card-title mb-3">Notification</h4>
        </div>
        <div class="col-sm-12" v-for="(data, index) in notificationData" :key="index">
          <iq-card>
            <template v-slot:body>
              <ul class="notification-list m-0 p-0">
                <li class="d-flex align-items-center justify-content-between">
                  <div class="user-img img-fluid">
                    <img :src="data.img" alt="story-img" class="rounded-circle avatar-40" />
                  </div>
                  <div class="w-100">
                    <div class="d-flex justify-content-between">
                      <div class="ms-3">
                        <h6>{{ data.heading }}</h6>
                        <p class="mb-0">{{ data.time }}</p>
                      </div>
                      <div class="d-flex align-items-center">
                        <a href="#" :class="data.iconbg">
                          <span class="btn-inner">
                            <i :class="data.iconclass">{{ data.iconname }}</i>
                          </span>
                        </a>

                        <div class="card-header-toolbar d-flex align-items-center">
                          <div class="dropdown">
                            <div class="dropdown-toggle" id="dropdownMenuButton" data-bs-toggle="dropdown"
                              aria-expanded="false" role="button">
                              <span class="material-symbols-outlined">
                                more_horiz
                              </span>
                            </div>
                            <div class="dropdown-menu dropdown-menu-right">
                              <a class="dropdown-item d-flex align-items-center" href="#"
                                v-for="(data, index) in action" :key="index">
                                <i :class="data.iconclass">{{
                                  data.iconname
                                  }}</i>{{ data.title }}</a>
                            </div>
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                </li>
              </ul>
            </template>
          </iq-card>
        </div>
      </div>
    </div>
  </div>
</template>
<script>

export default {
  name: "Notification",
  mounted() {
    const body = document.querySelector("body");
    body.classList.add("notification");
  },
  data() {
    return {
      seen: true,
      notificationData: [
        {
          img: require("../../../assets/images/user/01.jpg"),
          heading: "Paige Turner Posted in UI/UX Community",
          time: "30 minute ago",
          iconclass: "material-symbols-outlined md-18 font-size-16",
          iconname: "military_tech",
          iconbg: "btn btn-icon btn-primary-subtle btn-sm me-3",
        },
        {
          img: require("../../../assets/images/user/02.jpg"),
          heading: "Anne Fibbiyon Like Your Post",
          time: "1 hour ago",
          iconclass: "material-symbols-outlined md-18 font-size-16",
          iconname: "favorite_border",
          iconbg: "btn btn-icon btn-danger-subtle btn-sm me-3",
        },
        {
          img: require("../../../assets/images/user/03.jpg"),
          heading: "Barry Cuda add Story",
          time: "40 days ago",
          iconclass: "material-symbols-outlined md-18 font-size-16",
          iconname: "military_tech",
          iconbg: "btn btn-icon btn-primary-subtle btn-sm me-3",
        },
        {
          img: require("../../../assets/images/user/04.jpg"),
          heading: "Cliff Hanger posted a comment on your status update",
          time: "42 days ago",
          iconclass: "material-symbols-outlined font-size-16",
          iconname: "chat_bubble_outline",
          iconbg: "btn btn-icon btn-success-subtle btn-sm me-3",
        },
        {
          img: require("../../../assets/images/user/4.jpg"),
          heading: "Rick O'Shea posted a comment on your photo",
          time: "50 days ago",
          iconclass: "material-symbols-outlined font-size-16",
          iconname: "chat_bubble_outline",
          iconbg: "btn btn-icon btn-success-subtle btn-sm me-3",
        },
        {
          img: require("../../../assets/images/user/05.jpg"),
          heading: "Brock Lee Sent a Friend Request",
          time: "1 hour ago",
          iconclass: "material-symbols-outlined font-size-16",
          iconname: "reply",
          iconbg: "btn btn-icon me-3 btn-sm btn-warning-subtle",
        },
        {
          img: require("../../../assets/images/user/06.jpg"),
          heading: "Ira Membrit shared your status update",
          time: "1 hour ago",
          iconclass: "material-symbols-outlined font-size-16",
          iconname: "share",
          iconbg: "btn btn-icon me-3 btn-sm btn-warning-subtle",
        },
        {
          img: require("../../../assets/images/user/11.jpg"),
          heading: "Paul Molive and 3 ther have Birthday Today",
          time: "1 week, 1 day ago",
          iconclass: "material-symbols-outlined font-size-16",
          iconname: "cake",
          iconbg: "btn btn-icon me-3 btn-sm btn-danger-subtle",
        },
        {
          img: require("../../../assets/images/user/07.jpg"),
          heading: "Petey Cruiser Sent a Friend request",
          time: "1 day ago",
          iconclass: "material-symbols-outlined font-size-16",
          iconname: "reply",
          iconbg: "btn btn-icon me-3 btn-sm btn-warning-subtle",
        },
        {
          img: require("../../../assets/images/user/08.jpg"),
          heading: "Bob Frapples and 45 other Like Your Pst on timeline",
          time: "1 week ago",
          iconclass: "material-symbols-outlined font-size-16",
          iconname: "favorite_border",
          iconbg: "btn btn-icon me-3 btn-sm btn-danger-subtle",
        },
        {
          img: require("../../../assets/images/user/12.jpg"),
          heading: "Maya Didas share Your Post",
          time: "1 month  ago",
          iconclass: "material-symbols-outlined font-size-16",
          iconname: "share",
          iconbg: "btn btn-icon me-3 btn-sm btn-info-subtle",
        },
        {
          img: require("../../../assets/images/user/09.jpg"),
          heading: "Sal Monella Add Photo with You",
          time: "1 month ago",
          iconclass: "material-symbols-outlined font-size-16",
          iconname: "military_tech",
          iconbg: "btn btn-icon me-3 btn-sm btn-primary-subtle",
        },
        {
          img: require("../../../assets/images/user/10.jpg"),
          heading: "Barb Dwyer commented on your new profile status",
          time: "2 month ago",
          iconclass: "material-symbols-outlined font-size-16",
          iconname: "chat_bubble_outline",
          iconbg: "btn btn-icon me-3 btn-sm btn-success-subtle",
        },
        {
          img: require("../../../assets/images/user/13.jpg"),
          heading: "Terry Aki commented on your new profile status",
          time: "2 month  ago",
          iconclass: "material-symbols-outlined font-size-16",
          iconname: "chat_bubble_outline",
          iconbg: "btn btn-icon me-3 btn-sm btn-success-subtle",
        },
        {
          img: require("../../../assets/images/user/14.jpg"),
          heading: "Paige Turner Posted In Development Community",
          time: "3 month ago",
          iconclass: "material-symbols-outlined font-size-16",
          iconname: "military_tech",
          iconbg: "btn btn-icon me-3 btn-sm btn-primary-subtle",
        },
      ],
      action: [
        {
          iconclass: "material-symbols-outlined me-2 md-18",
          iconname: "visibility",
          title: "View",
        },
        {
          iconclass: "material-symbols-outlined me-2 md-18",
          iconname: "delete",
          title: "Delete",
        },
        {
          iconclass: "material-symbols-outlined me-2 md-18",
          iconname: "edit",
          title: "Edit",
        },
        {
          iconclass: "material-symbols-outlined me-2 md-18",
          iconname: "print",
          title: "Print",
        },
        {
          iconclass: "material-symbols-outlined me-2 md-18",
          iconname: "file_download",
          title: "Download",
        },
      ],
    };
  },
};
</script>
