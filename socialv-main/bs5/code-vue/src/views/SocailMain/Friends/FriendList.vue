<template>
  <div class="content-inner">
    <b-container>
      <b-row>
        <b-col md="6" v-for="(item, index) in friends" :key="index">
          <iq-card body-class="profile-page p-0 card-body">
            <template v-slot:body>
              <div class="profile-header-image">
                <div class="cover-container">
                  <img
                    :src="item.backgroudimg"
                    alt="profile-bg"
                    class="rounded img-fluid w-100"
                    loading="lazy"
                  />
                </div>
                <div class="profile-info p-4">
                  <div class="user-detail">
                    <div
                      class="d-flex flex-wrap justify-content-between align-items-start"
                    >
                      <div class="profile-detail d-flex">
                        <div class="profile-img pe-lg-4">
                          <img
                            :src="item.userimg"
                            alt="profile-img"
                            class="avatar-130 img-fluid"
                          />
                        </div>
                        <div class="user-data-block mt-md-0 mt-2">
                          <h4 class="text-primary">
                            <a href="/friendprofile"> {{ item.name }}</a>
                          </h4>
                          <h6>{{ item.desgination }}</h6>
                          <p :class="item.discclass">
                            Lorem Ipsum is simply dummy text of the
                          </p>
                        </div>
                      </div>
                      <button type="submit" class="btn btn-primary">
                        Following
                      </button>
                    </div>
                  </div>
                </div>
              </div>
            </template>
          </iq-card>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>
<script>
import { socialvue } from "../../../config/pluginInit";
export default {
  name: "FriendList",
  mounted() {
    socialvue.index();
  },
  data() {
    return {
      friends: [
        {
          name: "Anna Sthesia",
          desgination: "@designer",
          backgroudimg: require("../../../assets/images/page-img/profile-bg2.jpg"),
          userimg: require("../../../assets/images/user/05.jpg"),
          discclass: "mb-2 mb-md-0",
        },
        {
          name: "Paul Molive",
          desgination: "@developer",
          backgroudimg: require("../../../assets/images/page-img/profile-bg1.jpg"),
          userimg: require("../../../assets/images/user/06.jpg"),
          discclass: "mb-2 mb-md-0",
        },
        {
          name: "Anna Mull",
          desgination: "@designer",
          backgroudimg: require("../../../assets/images/page-img/profile-bg4.jpg"),
          userimg: require("../../../assets/images/user/07.jpg"),
          discclass: "mb-2 mb-md-0",
        },
        {
          name: "Paige Turner",
          desgination: "@tester",
          backgroudimg: require("../../../assets/images/page-img/profile-bg5.jpg"),
          userimg: require("../../../assets/images/user/08.jpg"),
          discclass: "mb-2 mb-md-0",
        },
        {
          name: "Bob Frapples",
          desgination: "@Developer",
          backgroudimg: require("../../../assets/images/page-img/profile-bg6.jpg"),
          userimg: require("../../../assets/images/user/09.jpg"),
          discclass: "mb-2 mb-md-0",
        },
        {
          name: "Barb Ackue",
          desgination: "@Grapfics",
          backgroudimg: require("../../../assets/images/page-img/profile-bg7.jpg"),
          userimg: require("../../../assets/images/user/10.jpg"),
          discclass: "mb-2 mb-md-0",
        },
        {
          name: "Greta Life",
          desgination: "@Fashion",
          backgroudimg: require("../../../assets/images/page-img/profile-bg8.jpg"),
          userimg: require("../../../assets/images/user/13.jpg"),
          discclass: "mb-2 mt-md-0",
        },
        {
          name: "Ira Membrit",
          desgination: "@designer",
          backgroudimg: require("../../../assets/images/page-img/profile-bg9.jpg"),
          userimg: require("../../../assets/images/user/14.jpg"),
          discclass: "mb-2 md-md-0",
        },
        {
          name: "Pete Sariya",
          desgination: "@Designer",
          backgroudimg: require("../../../assets/images/page-img/profile-bg1.jpg"),
          userimg: require("../../../assets/images/user/15.jpg"),
          discclass: "mb-2 mb-md-0",
        },
        {
          name: "Monty Carlo",
          desgination: "@designer",
          backgroudimg: require("../../../assets/images/page-img/profile-bg2.jpg"),
          userimg: require("../../../assets/images/user/16.jpg"),
          discclass: "mb-2 mb-md-0",
        },
        {
          name: "Ed Itorial",
          desgination: "@Testen",
          backgroudimg: require("../../../assets/images/page-img/profile-bg5.jpg"),
          userimg: require("../../../assets/images/user/17.jpg"),
          discclass: "mb-2 mb-md-0",
        },
        {
          name: "Paul Issy",
          desgination: "@R&D",
          backgroudimg: require("../../../assets/images/page-img/profile-bg8.jpg"),
          userimg: require("../../../assets/images/user/18.jpg"),
          discclass: "mb-2 mb-md-0",
        },
        {
          name: "Rick Shaw",
          desgination: "@Coder",
          backgroudimg: require("../../../assets/images/page-img/profile-bg7.jpg"),
          userimg: require("../../../assets/images/user/19.jpg"),
          discclass: "mb-2 mb-md-0",
        },
        {
          name: "Ben Effit",
          desgination: "@designer",
          backgroudimg: require("../../../assets/images/page-img/profile-bg9.jpg"),
          userimg: require("../../../assets/images/user/07.jpg"),
          discclass: "mb-2 mb-md-0",
        },
        {
          name: "Justin Case",
          desgination: "@designer",
          backgroudimg: require("../../../assets/images/page-img/profile-bg4.jpg"),
          userimg: require("../../../assets/images/user/08.jpg"),
          discclass: "mb-2 md-mb-0",
        },
        {
          name: "Aaron Ottix",
          desgination: "@designer",
          backgroudimg: require("../../../assets/images/page-img/profile-bg2.jpg"),
          userimg: require("../../../assets/images/user/09.jpg"),
          discclass: "mb-2 mb-mb-0",
        },
      ],
    };
  },
};
</script>
