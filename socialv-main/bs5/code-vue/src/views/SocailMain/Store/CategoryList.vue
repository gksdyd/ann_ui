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
            <b-card no-body>
              <div class="card-header d-flex justify-content-between">
                <div class="header-title">
                  <h4 class="card-title">Reviews</h4>
                </div>
              </div>
              <b-card-body class="pt-0">
                <div class="d-flex align-items-center justify-content-between mb-3">
                  <div class="form-check d-flex align-items-center">
                    <input type="radio" class="form-check-input" name="bsradio" id="radio1" checked="" />
                    <label for="radio1" class="mb-0 ps-2"><b>All Reviews</b></label>
                  </div>
                  <h6 class="text-primary">6870</h6>
                </div>
                <div class="d-flex align-items-center justify-content-between mb-2">
                  <div class="form-check d-inline-block">
                    <input type="radio" class="form-check-input" name="bsradio" id="radio1" checked="" />
                    <label for="radio1" class="form-check-label mb-0">
                      <span class="d-block line-height text-warning">
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i>
                      </span>
                    </label>
                  </div>
                  <h6 class="text-primary">1023</h6>
                </div>
                <div class="d-flex align-items-center justify-content-between mb-2">
                  <div class="form-check d-inline-block">
                    <input type="radio" name="bsradio" class="form-check-input" id="radio1" checked="" />
                    <label for="radio1" class="form-check-label mb-0">
                      <span class="d-block line-height text-warning">
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                        <i class="material-symbols-outlined md-18">star_half</i>
                      </span>
                    </label>
                  </div>
                  <h6 class="text-primary">1000</h6>
                </div>
                <div class="d-flex align-items-center justify-content-between mb-2">
                  <div class="form-check d-inline-block">
                    <input type="radio" name="bsradio" class="form-check-input" id="radio1" checked="" />
                    <label for="radio1" class="form-check-label mb-0">
                      <span class="d-block line-height text-warning">
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i>
                      </span>
                    </label>
                  </div>
                  <h6 class="text-primary">982</h6>
                </div>
                <div class="d-flex align-items-center justify-content-between mb-2">
                  <div class="form-check d-inline-block">
                    <input type="radio" name="bsradio" class="form-check-input" id="radio1" checked="" />
                    <label for="radio1" class="form-check-label mb-0">
                      <span class="d-block line-height text-warning">
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                        <i class="material-symbols-outlined md-18">star_half</i>
                      </span>
                    </label>
                  </div>
                  <h6 class="text-primary">204</h6>
                </div>
                <div class="d-flex align-items-center justify-content-between mb-2">
                  <div class="form-check d-inline-block">
                    <input type="radio" name="bsradio" class="form-check-input" id="radio1" checked="" />
                    <label for="radio1" class="form-check-label mb-0">
                      <span class="d-block line-height text-warning">
                        <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                        <i class="material-symbols-outlined md-18">star</i>
                      </span>
                    </label>
                  </div>
                  <h6 class="text-primary">50</h6>
                </div>
                <div class="d-flex align-items-center justify-content-between">
                  <div class="form-check d-inline-block">
                    <input type="radio" name="bsradio" class="form-check-input" id="radio1" checked="" />
                    <label for="radio1" class="form-check-label mb-0">
                      <span class="d-block line-height text-warning">
                        <i class="material-symbols-outlined md-18">star</i>
                      </span>
                    </label>
                  </div>
                  <h6 class="text-primary">8</h6>
                </div>
              </b-card-body>
            </b-card>
          </div>
        </b-col>
        <b-col lg="8">
          <b-row>
            <b-col md="12">
              <b-card no-body class="card-block card-stretch card-height product">
                <b-card-body>
                  <b-row v-for="(item, index) in products" :key="index" :class="`align-items-top ${item.mbclass}`">
                    <b-col lg="6">
                      <div class="image-block position-relative">
                        <img :src="item.imageSrc" class="img-fluid w-100 rounded" :alt="'product-img' + index"
                          loading="lazy" />
                        <div class="offer">
                          <div class="offer-title">20%</div>
                        </div>
                        <h6 class="price">
                          <span class="regular-price text-dark pr-2">{{
                            item.regularPrice
                          }}</span>{{ item.salePrice }}
                        </h6>
                      </div>
                    </b-col>
                    <b-col lg="6">
                      <div class="product-description ps-2 circle-category mt-2 mt-md-0">
                        <div class="d-flex align-items-center justify-content-between mb-3 border-bottom pb-3">
                          <div class="d-flex align-items-center">
                            <img class="img-fluid rounded-circle avatar-30" :src="item.userAvatar"
                              :alt="'user-avatar' + index" loading="lazy" />
                            <div class="ms-2">
                              <p class="mb-0 line-height">Posted By</p>
                              <h6>
                                <a :href="'#user-' + index">{{
                                  item.userName
                                }}</a>
                              </h6>
                            </div>
                          </div>
                          <div class="d-block line-height">
                            <span class="text-warning">
                              <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                              <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                              <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                              <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                              <i class="material-symbols-outlined md-18">star</i>
                            </span>
                          </div>
                        </div>
                        <a class="mb-1">{{ item.productName }}</a>
                        <p class="categry text-primary ps-3 mb-0 position-relative mb-0">
                          {{ item.category }}
                        </p>
                        <p class="mb-0">{{ item.description }}</p>
                      </div>
                    </b-col>
                  </b-row>
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
  name: "CategoryList",
  data() {
    return {
      products: [
        {
          mbclass: "mb-3",
          imageSrc: require("@/assets/images/store/01.jpg"),
          regularPrice: "$87.00",
          salePrice: "$75.00",
          userAvatar: require("@/assets/images/user/01.jpg"),
          userName: "Bearded Wonder",
          productName: "Flaming Skull Team Logo",
          category: "Logo and badges",
          description:
            "Success in containing the virus comes slowing activity.",
        },
        {
          mbclass: "mb-3",
          imageSrc: require("@/assets/images/store/02.jpg"),
          regularPrice: "$87.00",
          salePrice: "$75.00",
          userAvatar: require("@/assets/images/user/02.jpg"),
          userName: "Bearded Wonder",
          productName: "Flaming Skull Team Logo",
          category: "Logo and badges",
          description:
            "Success in containing the virus comes slowing activity.",
        },
        {
          mbclass: "mb-3",
          imageSrc: require("@/assets/images/store/03.jpg"),
          regularPrice: "$87.00",
          salePrice: "$75.00",
          userAvatar: require("@/assets/images/user/01.jpg"),
          userName: "Bearded Wonder",
          productName: "Flaming Skull Team Logo",
          category: "Logo and badges",
          description:
            "Success in containing the virus comes slowing activity.",
        },
        {
          mbclass: "mb-3",
          imageSrc: require("@/assets/images/store/04.jpg"),
          regularPrice: "$87.00",
          salePrice: "$75.00",
          userAvatar: require("@/assets/images/user/01.jpg"),
          userName: "Bearded Wonder",
          productName: "Flaming Skull Team Logo",
          category: "Logo and badges",
          description:
            "Success in containing the virus comes slowing activity.",
        },
        {
          mbclass: "mb-3",
          imageSrc: require("@/assets/images/store/05.jpg"),
          regularPrice: "$87.00",
          salePrice: "$75.00",
          userAvatar: require("@/assets/images/user/01.jpg"),
          userName: "Bearded Wonder",
          productName: "Flaming Skull Team Logo",
          category: "Logo and badges",
          description:
            "Success in containing the virus comes slowing activity.",
        },
        {
          mbclass: "mb-3",
          imageSrc: require("@/assets/images/store/06.jpg"),
          regularPrice: "$87.00",
          salePrice: "$75.00",
          userAvatar: require("@/assets/images/user/01.jpg"),
          userName: "Bearded Wonder",
          productName: "Flaming Skull Team Logo",
          category: "Logo and badges",
          description:
            "Success in containing the virus comes slowing activity.",
        },
        {
          mbclass: "mb-3",
          imageSrc: require("@/assets/images/store/07.jpg"),
          regularPrice: "$87.00",
          salePrice: "$75.00",
          userAvatar: require("@/assets/images/user/01.jpg"),
          userName: "Bearded Wonder",
          productName: "Flaming Skull Team Logo",
          category: "Logo and badges",
          description:
            "Success in containing the virus comes slowing activity.",
        },
        {
          mbclass: "",
          imageSrc: require("@/assets/images/store/08.jpg"),
          regularPrice: "$87.00",
          salePrice: "$75.00",
          userAvatar: require("@/assets/images/user/01.jpg"),
          userName: "Bearded Wonder",
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
