<template>
  <div class="content-inner">
    <div class="container">
      <div class="row">
        <div class="col-sm-12">
          <div class="birthday-block" v-for="(birth, index) in birthdate" :key="index">
            <iq-card>
              <template v-slot:headerTitle>
                <h4 class="card-title">{{ birth.name }}</h4>
              </template>
            </iq-card>
            <div class="row">
              <div class="col-md-12 col-lg-6" v-for="(img, index1) in birth.image" :key="index1">
                <b-card no-body>
                  <b-card-body>
                    <div class="iq-birthday-block">
                      <div class="d-flex align-items-center justify-content-between">
                        <div class="d-flex align-items-center">
                          <b-link href="#">
                            <b-img :src="img.img" alt="profile-img" class="img-fluid" />
                          </b-link>
                          <div class="friend-info ms-0 ms-md-3 mt-md-0 mt-2">
                            <h5>{{ img.title }}</h5>
                            <p class="mb-0">{{ img.text }}</p>
                          </div>
                        </div>
                        <button class="btn btn-primary">Create Card</button>
                      </div>
                    </div>
                  </b-card-body>
                </b-card>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
// import { socialvue } from '../../../config/pluginInit'
export default {
  name: "Birthdate",
  mounted() {
    // socialvue.index()
  },
  data() {
    return {
      birthdate: [
        {
          name: "Today Birthday",
          image: [
            {
              title: "Petey Cruiser",
              text: "Today",
              img: require("../../../assets/images/user/05.jpg"),
            },
            {
              title: "Petey Cruiser",
              text: "Today",
              img: require("../../../assets/images/user/06.jpg"),
            },
          ],
        },
        {
          name: "Upcoming Birthday",
          image: [
            {
              title: "Petey Cruiser",
              text: "Tomorrow",
              img: require("../../../assets/images/user/07.jpg"),
            },
            {
              title: "Paul Molive",
              text: "Tomorrow",
              img: require("../../../assets/images/user/08.jpg"),
            },
          ],
        },
        {
          name: "January Birthday",
          image: [
            {
              title: "Paige Turner",
              text: "02-jan-2020",
              img: require("../../../assets/images/user/09.jpg"),
            },
            {
              title: "Bob Frapples",
              text: "15-jan-2020",
              img: require("../../../assets/images/user/10.jpg"),
            },
            {
              title: "Barb Ackue",
              text: "15-jan-2020",
              img: require("../../../assets/images/user/13.jpg"),
            },
          ],
        },
        {
          name: "February Birthday",
          image: [
            {
              title: "Greta Life",
              text: "01-feb-2020",
              img: require("../../../assets/images/user/14.jpg"),
            },
          ],
        },
        {
          name: "March Birthday",
          image: [
            {
              title: "Ira Membrit",
              text: "01-Mar-2020",
              img: require("../../../assets/images/user/15.jpg"),
            },
            {
              title: "Pete Sariya",
              text: "5-Mar-2020",
              img: require("../../../assets/images/user/16.jpg"),
            },
            {
              title: "Monty Carlo",
              text: "20-Mar-2020",
              img: require("../../../assets/images/user/17.jpg"),
            },
            {
              title: "Ed Itorial",
              text: "30-Mar-2020",
              img: require("../../../assets/images/user/18.jpg"),
            },
          ],
        },
        {
          name: "April Birthday",
          image: [
            {
              title: "Paul Issy",
              text: "06-Apr-2020",
              img: require("../../../assets/images/user/19.jpg"),
            },
            {
              title: "Rick Shaw",
              text: "12-Apr-2020",
              img: require("../../../assets/images/user/07.jpg"),
            },
            {
              title: "Ben Effit",
              text: "18-Apr-2020",
              img: require("../../../assets/images/user/08.jpg"),
            },
          ],
        },
        {
          name: "May Birthday",
          image: [
            {
              title: "Justin Case",
              text: "03-May-2020",
              img: require("../../../assets/images/user/09.jpg"),
            },
            {
              title: "Aaron Ottix",
              text: "4-May-2020",
              img: require("../../../assets/images/user/10.jpg"),
            },
            {
              title: "Pete Sariya",
              text: "15-May-2020",
              img: require("../../../assets/images/user/13.jpg"),
            },
          ],
        },
      ],
    };
  },
};
</script>
