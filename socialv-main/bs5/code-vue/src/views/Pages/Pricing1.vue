<template>
  <div class="content-inner">
    <b-container>
      <b-row>
        <b-col sm="12">
          <b-card no-body class="position-relative inner-page-bg bg-primary" style="height: 150px">
            <div class="inner-page-title">
              <h3 class="text-white">Pricing 2</h3>
              <p class="text-white">lorem ipsum</p>
            </div>
          </b-card>
        </b-col>
        <b-col lg="3" md="6" sm="12" v-for="(item, index) in cards" :key="index">
          <b-card no-body :class="item.active ? 'bg-primary text-white' : ''">
            <div class="card-body border text-center rounded">
              <span class="text-uppercase" v-if="item.plan !== ''">{{
                item.plan
                }}</span>
              <div class="d-flex align-items-center justify-content-center">
                <h2 class="mb-4 display-3" :class="item.active ? 'text-white' : ''">
                  {{ item.amount }}
                </h2>
                <small class="text-muted" :class="item.active ? 'text-white-50' : 'text-muted'">{{ item.duration
                  }}</small>
              </div>
              <ul class="list-unstyled line-height-4 mb-0">
                <li>{{ item.description }}</li>
                <li>{{ item.description1 }}</li>
                <li>{{ item.description2 }}</li>
              </ul>
              <a href="#" :class="item.active
                ? 'btn btn-light  btn-block mt-5' + ' ' + item.buttonClass
                : 'btn btn-primary mt-5' + ' ' + item.buttonClass
                ">{{ item.button }}</a>
            </div>
          </b-card>
        </b-col>
        <b-col lg="3" md="6" sm="12" v-for="(item, index) in bgCards" :key="item.amount + index">
          <div class="card bg-dark text-white text-center">
            <img :src="item.bgImage" class="card-img rounded" alt="#" />
            <div class="card-img-overlay">
              <div class="d-flex align-items-center justify-content-center">
                <h2 class="mb-4 display-3 text-white">{{ item.amount }}</h2>
                <small class="text-white">{{ item.duration }}</small>
              </div>
              <ul class="list-unstyled line-height-4 mb-0">
                <li>{{ item.description }}</li>
                <li>{{ item.description1 }}</li>
                <li>{{ item.description2 }}</li>
              </ul>
              <button type="button" class="btn btn-primary mt-3">
                {{ item.button }}
              </button>
            </div>
          </div>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>
<script>

export default {
  name: "Pricing1",
  mounted() {
  },
  data() {
    return {
      cards: [
        {
          plan: "Basic",
          amount: "$26",
          duration: "/ Month",
          active: false,
          description: "Lorem ipsum dolor sit amet",
          description1: "Consectetur adipiscing elit",
          description2: "Integer molestie lorem at massa",
          button: "Start Starter",
          buttonClass: "",
          bgImage: false,
        },
        {
          plan: "Basic",
          amount: "$99",
          duration: "/ Month",
          active: true,
          description: "Lorem ipsum dolor sit amet",
          description1: "Consectetur adipiscing elit",
          description2: "Integer molestie lorem at massa",
          button: "Start Starter",
          buttonClass: "btn-block",
          bgImage: false,
        },
        {
          plan: "Basic",
          amount: "$39",
          duration: "/ Month",
          active: false,
          description: "Lorem ipsum dolor sit amet",
          description1: "Consectetur adipiscing elit",
          description2: "Integer molestie lorem at massa",
          button: "Start Starter",
          buttonClass: "",
          bgImage: false,
        },
        {
          plan: "Basic",
          amount: "$25",
          duration: "/ Month",
          active: false,
          description: "Lorem ipsum dolor sit amet",
          description1: "Consectetur adipiscing elit",
          description2: "Integer molestie lorem at massa",
          button: "Start Starter",
          buttonClass: "",
          bgImage: false,
        },
      ],
      bgCards: [
        {
          amount: "$19",
          duration: "/ Month",
          active: false,
          description: "Lorem ipsum dolor sit amet",
          description1: "Consectetur adipiscing elit",
          description2: "Integer molestie lorem at massa",
          button: "Get started",
          buttonClass: "",
          bgImage: require("@/assets/images/page-img/25.jpg"),
        },
        {
          amount: "$19",
          duration: "/ Month",
          active: false,
          description: "Lorem ipsum dolor sit amet",
          description1: "Consectetur adipiscing elit",
          description2: "Integer molestie lorem at massa",
          button: "Get started",
          buttonClass: "",
          bgImage: require("@/assets/images/page-img/26.jpg"),
        },
        {
          amount: "$19",
          duration: "/ Month",
          active: false,
          description: "Lorem ipsum dolor sit amet",
          description1: "Consectetur adipiscing elit",
          description2: "Integer molestie lorem at massa",
          button: "Get started",
          buttonClass: "",
          bgImage: require("@/assets/images/page-img/27.jpg"),
        },
        {
          amount: "$19",
          duration: "/ Month",
          active: false,
          description: "Lorem ipsum dolor sit amet",
          description1: "Consectetur adipiscing elit",
          description2: "Integer molestie lorem at massa",
          button: "Get started",
          buttonClass: "",
          bgImage: require("@/assets/images/page-img/28.jpg"),
        },
      ],
    };
  },
};
</script>
