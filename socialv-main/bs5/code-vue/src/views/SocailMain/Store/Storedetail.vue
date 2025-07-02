<template>
  <div class="content-inner">
    <b-container>
      <b-row>
        <b-col lg="12">
          <b-card no-body>
            <b-card-header class="d-flex justify-content-between border-bottom">
              <div class="header-title">
                <b-card-title>Store Categories</b-card-title>
              </div>
            </b-card-header>
            <b-card-body>
              <b-row>
                <b-col
                  sm="6"
                  md="6"
                  lg="3"
                  class="mb-md-2 mb-2"
                  v-for="(category, index) in categories"
                  :key="index"
                >
                  <router-link :to="{ name: 'store.category-grid' }">
                    <b-img
                      :src="category.image"
                      alt="category-image"
                      fluid
                      rounded
                    />
                  </router-link>
                </b-col>
              </b-row>
            </b-card-body>
          </b-card>
        </b-col>
        <b-col lg="12">
          <b-card no-body class="shadow-none p-0">
            <b-card-header class="d-flex justify-content-between">
              <div class="header-title">
                <b-card-title class="card-title">Store Categories</b-card-title>
              </div>
            </b-card-header>
          </b-card>
          <b-row>
            <b-col
              sm="6"
              md="6"
              lg="4"
              v-for="(product, index) in products"
              :key="index"
            >
              <b-card no-body class="card-stretch card-height product">
                <b-card-body>
                  <div
                    class="d-flex align-items-center justify-content-between pb-3"
                  >
                    <div class="d-flex align-items-center">
                      <img
                        :src="product.userAvatar"
                        alt="User Avatar"
                        class="img-fluid rounded-circle avatar-30"
                        loading="lazy"
                      />
                      <div class="media-body ms-2">
                        <p class="mb-0 line-height">Posted By</p>
                        <h6>
                          <a href="#">{{ product.userName }}</a>
                        </h6>
                      </div>
                    </div>
                    <div class="d-block line-height">
                      <span class="text-warning">
                        <i class="material-symbols-outlined md-18">star</i
                        >{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i
                        >{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i
                        >{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i
                        >{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i>
                      </span>
                    </div>
                  </div>
                  <div class="image-block position-relative">
                    <img
                      :src="product.productImage"
                      class="img-fluid w-100 rounded"
                      alt="product-img"
                    />
                    <div
                      class="offer"
                      :class="{
                        'bg-danger': product.offer === '50%',
                      }"
                    >
                      <div class="offer-title">
                        {{ product.offer }}
                      </div>
                    </div>
                    <h6 class="price">
                      <span class="regular-price text-dark pr-2">$87.00</span
                      >$75.00
                    </h6>
                  </div>
                  <div class="product-description mt-3">
                    <a class="mb-1">Flaming Skull Team Logo</a>
                    <p
                      class="categry text-primary ps-3 mb-0 position-relative mb-0"
                    >
                      Logo and badges
                    </p>
                    <p class="mb-0">
                      Success in containing the virus comes slowing activity.
                    </p>
                  </div>
                </b-card-body>
              </b-card>
            </b-col>
          </b-row>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>
<script>
export default {
  name: "Storedetail",
  data() {
    return {
      categories: [
        { image: require("@/assets/images/store/c1.jpg") },
        { image: require("@/assets/images/store/c2.jpg") },
        { image: require("@/assets/images/store/c3.jpg") },
        { image: require("@/assets/images/store/c4.jpg") },
      ],
      products: [
        {
          userName: "Bearded Wonder",
          userAvatar: require("@/assets/images/user/01.jpg"),
          productImage: require("@/assets/images/store/01.jpg"),
          offer: "30%",
        },
        {
          userName: "Paul Molive",
          userAvatar: require("@/assets/images/user/02.jpg"),
          productImage: require("@/assets/images/store/02.jpg"),
          offer: "30%",
        },
        {
          userName: "Anna Mull",
          userAvatar: require("@/assets/images/user/03.jpg"),
          productImage: require("@/assets/images/store/03.jpg"),
          offer: "50%",
        },
        {
          userName: "Terry Aki",
          userAvatar: require("@/assets/images/user/04.jpg"),
          productImage: require("@/assets/images/store/04.jpg"),
          offer: "30%",
        },
        {
          userName: "Rock Lai",
          userAvatar: require("@/assets/images/user/05.jpg"),
          productImage: require("@/assets/images/store/05.jpg"),
          offer: "20%",
        },
        {
          userName: "Cliff Hanger",
          userAvatar: require("@/assets/images/user/06.jpg"),
          productImage: require("@/assets/images/store/06.jpg"),
          offer: "40%",
        },
        {
          userName: "Pete Sariya",
          userAvatar: require("@/assets/images/user/07.jpg"),
          productImage: require("@/assets/images/store/07.jpg"),
          offer: "50%",
        },
        {
          userName: "Alex John",
          userAvatar: require("@/assets/images/user/08.jpg"),
          productImage: require("@/assets/images/store/08.jpg"),
          offer: "30%",
        },
        {
          userName: "Paige Turner",
          userAvatar: require("@/assets/images/user/09.jpg"),
          productImage: require("@/assets/images/store/09.jpg"),
          offer: "10%",
        },
      ],
    };
  },
};
</script>
