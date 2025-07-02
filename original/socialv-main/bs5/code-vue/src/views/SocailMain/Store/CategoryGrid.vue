<template>
  <div class="content-inner">
    <b-container>
      <b-row>
        <b-col lg="4">
          <div class="fixed-suggestion mb-4">
            <b-card no-body>
              <div class="card-header d-flex justify-content-between">
                <div class="header-title">
                  <h4 class="card-title">Store Categories</h4>
                </div>
              </div>
              <b-card-body class="pt-0">
                <div class="form-check d-block mb-2">
                  <input type="checkbox" class="form-check-input" id="customCheck1" />
                  <label class="form-check-label" for="customCheck1">All Categories</label>
                </div>
                <div class="form-check d-block mb-2">
                  <input type="checkbox" class="form-check-input" id="customCheck2" />
                  <label class="form-check-label" for="customCheck2">PSD Templates</label>
                </div>
                <div class="form-check d-block mb-2">
                  <input type="checkbox" class="form-check-input" id="customCheck3" />
                  <label class="form-check-label" for="customCheck3">HTML Templates</label>
                </div>
                <div class="form-check d-block mb-2">
                  <input type="checkbox" class="form-check-input" id="customCheck4" />
                  <label class="form-check-label" for="customCheck4">WP Templates</label>
                </div>
                <div class="form-check d-block mb-2">
                  <input type="checkbox" class="form-check-input" id="customCheck5" />
                  <label class="form-check-label" for="customCheck5">Stream Packs</label>
                </div>
                <div class="form-check d-block">
                  <input type="checkbox" class="form-check-input" id="customCheck6" />
                  <label class="form-check-label" for="customCheck6">Logos and Badges</label>
                </div>
              </b-card-body>
            </b-card>
            <b-card no-body>
              <div class="card-header d-flex justify-content-between">
                <div class="header-title">
                  <h4 class="card-title">Price Range</h4>
                </div>
              </div>
              <b-card-body class="pt-0">
                <div class="d-flex align-items-center">
                  <div class="form-group me-3">
                    <label for="from">From:</label>
                    <input type="text" class="form-control" id="form" value="$  " />
                  </div>
                  <div class="form-group">
                    <label for="to">To:</label>
                    <input type="text" class="form-control" id="to" value="$  " />
                  </div>
                </div>
                <button type="submit" class="btn btn-primary w-100">Apply</button>
              </b-card-body>
            </b-card>
            <div class="card">
              <div class="card-header d-flex justify-content-between">
                <div class="header-title">
                  <h4 class="card-title">Reviews</h4>
                </div>
              </div>
              <div class="card-body pt-0">
                <div class="d-flex align-items-center justify-content-between mb-3">
                  <div class="form-check d-flex align-items-center">
                    <input type="radio" class="form-check-input" name="bsradio" id="radio1" checked="">
                    <label for="radio1" class="form-check-label mb-0 ps-2"><b>All Reviews</b></label>
                  </div>
                  <h6 class="text-primary">6870</h6>
                </div>
                <div class="d-flex align-items-center justify-content-between mb-2">
                  <div class="form-check d-inline-block">
                    <input type="radio" class="form-check-input" name="bsradio" id="radio2" checked="">
                    <label for="radio2" class="form-check-label mb-0">
                      <span class=" text-warning d-block line-height">
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                      </span>
                    </label>
                  </div>
                  <h6 class="text-primary">1023</h6>
                </div>
                <div class="d-flex align-items-center justify-content-between mb-2">
                  <div class="form-check d-inline-block">
                    <input type="radio" class="form-check-input" name="bsradio" id="radio3" checked="">
                    <label for="radio3" class="form-check-label mb-0">
                      <span class="text-warning d-block line-height">
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                      </span>
                    </label>
                  </div>
                  <h6 class="text-primary">1000</h6>
                </div>
                <div class="d-flex align-items-center justify-content-between mb-2">
                  <div class="form-check d-inline-block">
                    <input type="radio" class="form-check-input" name="bsradio" id="radio4" checked="">
                    <label for="radio4" class="form-check-label  mb-0">
                      <span class="text-warning d-block line-height">
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                      </span>
                    </label>
                  </div>
                  <h6 class="text-primary">982</h6>
                </div>
                <div class="d-flex align-items-center justify-content-between mb-2">
                  <div class="form-check d-inline-block">
                    <input type="radio" class="form-check-input" name="bsradio" id="radio5" checked="">
                    <label for="radio5" class="form-check-label mb-0">
                      <span class="text-warning d-block line-height">
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                      </span>
                    </label>
                  </div>
                  <h6 class="text-primary">204</h6>
                </div>
                <div class="d-flex align-items-center justify-content-between mb-2">
                  <div class="form-check d-inline-block">
                    <input type="radio" class="form-check-input" name="bsradio" id="radio6" checked="">
                    <label for="radio6" class="form-check-label mb-0">
                      <span class="text-warning d-block line-height">
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                      </span>
                    </label>
                  </div>
                  <h6 class="text-primary">50</h6>
                </div>
                <div class="d-flex align-items-center justify-content-between">
                  <div class="form-check d-inline-block">
                    <input type="radio" class="form-check-input" name="bsradio" id="radio7" checked="">
                    <label for="radio7" class="orm-check-label mb-0">
                      <span class="text-warning d-block line-height">
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                      </span>
                    </label>
                  </div>
                  <h6 class="text-primary">8</h6>
                </div>
              </div>
            </div>
          </div>
        </b-col>
        <b-col lg="8">
          <b-row>
            <!-- Loop through product data -->
            <b-col v-for="(product, index) in products" :key="index" sm="6" md="6">
              <b-card no-body class="card-block card-stretch card-height product">
                <b-card-body>
                  <div class="d-flex align-items-center justify-content-between pb-3">
                    <div class="d-flex align-items-center">
                      <img class="img-fluid rounded-circle avatar-30" :src="product.userAvatar" alt="" />
                      <div class="media-body ms-2">
                        <p class="mb-0 line-height">Posted By</p>
                        <h6>
                          <a href="#">{{ product.userName }}</a>
                        </h6>
                      </div>
                    </div>
                    <div class="d-block line-height">
                      <span class="font-size-11 text-warning">
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i>
                      </span>
                    </div>
                  </div>
                  <div class="image-block position-relative">
                    <img :src="product.productImage" class="img-fluid w-100 rounded" alt="product-img" />
                    <div class="offer" :class="{
                      'bg-danger': product.offerPercentage === '50%',
                    }">
                      <div class="offer-title">
                        {{ product.offerPercentage }}
                      </div>
                    </div>
                    <h6 class="price">
                      <span class="regular-price text-dark pr-2">{{
                        product.regularPrice
                        }}</span>{{ product.discountedPrice }}
                    </h6>
                  </div>
                  <div class="product-description mt-3">
                    <a class="mb-1">{{ product.productName }}</a>
                    <p class="categry text-primary ps-3 mb-0 position-relative mb-0">
                      {{ product.category }}
                    </p>
                    <p class="mb-0">{{ product.description }}</p>
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
  name: "CategoryGrid",
  data() {
    return {
      products: [
        {
          userAvatar: require("@/assets/images/user/01.jpg"),

          userName: "Paul Molive",
          productImage: require("@/assets/images/store/01.jpg"),
          offerPercentage: "30%",
          regularPrice: "$87.00",
          discountedPrice: "$75.00",
          productName: "Flaming Skull Team Logo",
          category: "Logo and badges",
          description:
            "Success in containing the virus comes slowing activity.",
        },
        {
          userAvatar: require("@/assets/images/user/02.jpg"),

          userName: "Paul Molive",
          productImage: require("@/assets/images/store/02.jpg"),
          offerPercentage: "30%",
          regularPrice: "$87.00",
          discountedPrice: "$75.00",
          productName: "Flaming Skull Team Logo",
          category: "Logo and badges",
          description:
            "Success in containing the virus comes slowing activity.",
        },
        {
          userAvatar: require("@/assets/images/user/03.jpg"),

          userName: "Anna Mull",
          productImage: require("@/assets/images/store/03.jpg"),
          offerPercentage: "50%",
          regularPrice: "$87.00",
          discountedPrice: "$75.00",
          productName: "Flaming Skull Team Logo",
          category: "Logo and badges",
          description:
            "Success in containing the virus comes slowing activity.",
        },
        {
          userAvatar: require("@/assets/images/user/04.jpg"),

          userName: "Terry Aki",
          productImage: require("@/assets/images/store/04.jpg"),
          offerPercentage: "30%",
          regularPrice: "$87.00",
          discountedPrice: "$75.00",
          productName: "Flaming Skull Team Logo",
          category: "Logo and badges",
          description:
            "Success in containing the virus comes slowing activity.",
        },
        {
          userAvatar: require("@/assets/images/user/05.jpg"),

          userName: "Rock Lai",
          productImage: require("@/assets/images/store/05.jpg"),
          offerPercentage: "20%",
          regularPrice: "$87.00",
          discountedPrice: "$75.00",
          productName: "Flaming Skull Team Logo",
          category: "Logo and badges",
          description:
            "Success in containing the virus comes slowing activity.",
        },
        {
          userAvatar: require("@/assets/images/user/06.jpg"),

          userName: "Cliff Hanger",
          productImage: require("@/assets/images/store/06.jpg"),
          offerPercentage: "40%",
          regularPrice: "$87.00",
          discountedPrice: "$75.00",
          productName: "Flaming Skull Team Logo",
          category: "Logo and badges",
          description:
            "Success in containing the virus comes slowing activity.",
        },
        {
          userAvatar: require("@/assets/images/user/07.jpg"),

          userName: "Pete Sariya",
          productImage: require("@/assets/images/store/07.jpg"),
          offerPercentage: "50%",
          regularPrice: "$87.00",
          discountedPrice: "$75.00",
          productName: "Flaming Skull Team Logo",
          category: "Logo and badges",
          description:
            "Success in containing the virus comes slowing activity.",
        },
        {
          userAvatar: require("@/assets/images/user/08.jpg"),

          userName: "Alex John",
          productImage: require("@/assets/images/store/08.jpg"),
          offerPercentage: "30%",
          regularPrice: "$87.00",
          discountedPrice: "$75.00",
          productName: "Flaming Skull Team Logo",
          category: "Logo and badges",
          description:
            "Success in containing the virus comes slowing activity.",
        },
      ],
    };
  },
};
</script>
