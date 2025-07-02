<template>
  <div class="content-inner">
    <div class="container">
      <div class="d-grid gap-3 d-grid-template-1fr-19">
        <div v-for="(event, index) in profileEvent" :key="index" class="card rounded" :class="event.class">
          <div class="event-images">
            <a href="#">
              <img :src="event.backgroudimg" class="img-fluid" alt="Responsive image" />
            </a>
          </div>
          <div class="card-body">
            <div class="d-flex">
              <div class="date-of-event">
                <span>{{ event.month }}</span>
                <h5>{{ event.date }}</h5>
              </div>
              <div class="events-detail ms-3">
                <h5>
                  <router-link :to="{ name: 'social.event-detail' }">{{ event.name }}</router-link>
                </h5>
                <p>Lorem Ipsum is simply dummy text</p>
                <div class="event-member">
                  <div class="iq-media-group">
                    <a href="#" class="iq-media">
                      <img class="img-fluid avatar-40 rounded-circle" src="@/assets/images/user/05.jpg" alt=""
                        loading="lazy">
                    </a>{{ "" }}
                    <a href="#" class="iq-media">
                      <img class="img-fluid avatar-40 rounded-circle" src="@/assets/images/user/06.jpg" alt=""
                        loading="lazy">
                    </a>{{ "" }}
                    <a href="#" class="iq-media">
                      <img class="img-fluid avatar-40 rounded-circle" src="@/assets/images/user/07.jpg" alt=""
                        loading="lazy">
                    </a>{{ "" }}
                    <a href="#" class="iq-media">
                      <img class="img-fluid avatar-40 rounded-circle" src="@/assets/images/user/08.jpg" alt=""
                        loading="lazy">
                    </a>{{ "" }}
                    <a href="#" class="iq-media">
                      <img class="img-fluid avatar-40 rounded-circle" src="@/assets/images/user/09.jpg" alt=""
                        loading="lazy">
                    </a>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProfileEvent",
  data() {
    return {
      profileEvent: [
        {
          name: "New Year Celebration",
          backgroudimg: require("../../../assets/images/page-img/51.jpg"),
          month: "Jan",
          date: "01",
          class: "mb-0"
        },
        {
          name: "Birthday Celebration",
          backgroudimg: require("../../../assets/images/page-img/52.jpg"),
          month: "Jan",
          date: "24",
          class: "mb-0"
        },
        {
          name: "Republic day",
          backgroudimg: require("../../../assets/images/page-img/53.jpg"),
          month: "Jan",
          date: "26",
          class: "mb-0"
        },
        {
          name: "Meetings & Conventions",
          backgroudimg: require("../../../assets/images/page-img/54.jpg"),
          month: "Feb",
          date: "04",
          class: "mb-0"
        },
        {
          name: "Fun Events and Festivals",
          backgroudimg: require("../../../assets/images/page-img/55.jpg"),
          month: "Mar",
          date: "01",
          class: "mb-0"
        },
        {
          name: "Atlanta Retail Show",
          backgroudimg: require("../../../assets/images/page-img/56.jpg"),
          month: "Mar",
          date: "10",
          class: "mb-0"
        },
        {
          name: "Holi in the City",
          backgroudimg: require("../../../assets/images/page-img/57.jpg"),
          month: "Mar",
          date: "14",

        },
        {
          name: "Insurance Innovators",
          backgroudimg: require("../../../assets/images/page-img/58.jpg"),
          month: "Mar",
          date: "16",
        },
        {
          name: "BIG 5G Event",
          backgroudimg: require("../../../assets/images/page-img/59.jpg"),
          month: "Apr",
          date: "12",
        },
      ],
    };
  },
};

</script>

<style scoped>
/* Add your custom styles here */
</style>
