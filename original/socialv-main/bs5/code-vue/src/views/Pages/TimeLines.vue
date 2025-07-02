<template>
  <div class="content-inner">
    <div class="container">
      <div class="row">
        <div class="col-sm-12">
          <div
            class="card position-relative inner-page-bg bg-primary"
            style="height: 150px"
          >
            <div class="inner-page-title">
              <h3 class="text-white">Timeline Page</h3>
              <p class="text-white">lorem ipsum</p>
            </div>
          </div>
        </div>
        <div class="col-lg-6">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Product Orders</h4>
            </template>
            <template v-slot:body>
              <TimeLine :items="timelineItems" />
            </template>
          </iq-card>
        </div>
        <div class="col-lg-6">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Product Orders</h4>
            </template>
            <template v-slot:body>
              <TimeLine :items="timelineItems" />
            </template>
          </iq-card>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
// import { socialvue } from '../../config/pluginInit'

export default {
  name: "TimeLines",
  mounted() {
    // socialvue.index()
  },
  data() {
    return {
      timelineItems: [
        {
          color: "primary",
          title: "Client Login",
          right: "24 November 2019",
          description:
            "Bonbon macaroon jelly beans gummi bears jelly lollipop apple",
          child: {
            type: "img",
            items: [],
          },
        },
        {
          color: "success",
          title: "Scheduled Maintenance",
          right: "23 November 2019",
          description:
            "Bonbon macaroon jelly beans gummi bears jelly lollipop apple",
          child: {
            type: "img",
            items: [],
          },
        },
        {
          color: "danger",
          title: "Dev Meetup",
          right: "20 November 2019",
          description:
            'Bonbon macaroon jelly beans<a href=""> gummi bears</a>gummi bears jelly lollipop apple',
          child: {
            type: "img",
            items: [
              require("../../assets/images/user/01.jpg"),
              require("../../assets/images/user/02.jpg"),
              require("../../assets/images/user/user-6.jpg"),
              require("../../assets/images/user/user-3.jpg"),
              require("../../assets/images/user/user-1.jpg"),
              require("../../assets/images/user/user-2.jpg"),
            ],
          },
        },
        {
          color: "primary",
          title: "Client Call",
          right: "19 November 2019",
          description:
            "Bonbon macaroon jelly beans gummi bears jelly lollipop apple",
          child: {
            type: "img",
            items: [],
          },
        },
        {
          color: "info",
          title: "Mega Event",
          right: "15 November 2019",
          description:
            "Bonbon macaroon jelly beans gummi bears jelly lollipop apple",
          child: {
            type: "img",
            items: [],
          },
        },
        {
          color: "info",
          title: "Client Call",
          right: "19 November 2019",
          description:
            "Bonbon macaroon jelly beans gummi bears jelly lollipop apple",
          child: {
            type: "img",
            items: [],
          },
        },
        {
          color: "warning",
          title: "Mega Event",
          right: "15 November 2019",
          description:
            "Bonbon macaroon jelly beans gummi bears jelly lollipop apple",
          child: {
            type: "img",
            items: [],
          },
        },
        {
          color: "info",
          title: "Client Call",
          right: "19 November 2019",
          description:
            "Bonbon macaroon jelly beans gummi bears jelly lollipop apple",
          child: {
            type: "img",
            items: [],
          },
        },
      ],
    };
  },
};
</script>
