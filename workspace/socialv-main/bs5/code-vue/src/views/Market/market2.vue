<template>
  <div class="content-inner">
    <div class="container">
      <div class="row">
        <b-col lg="4">
          <b-card no-body>
            <div class="top-bg-image">
              <b-img :src="require('@/assets/images/page-img/59.jpg')" class="img-fluid" alt="Responsive image"
                loading="lazy" />
            </div>
            <div class="card-body text-center">
              <div class="group-icon">
                <b-img :src="require('@/assets/images/user/11.png')" alt="profile-img" class="avatar-100 img-fluid"
                  loading="lazy" />
              </div>
              <h3 class="text-center mt-2">Roy</h3>
              <h6>
                098hgdvb53562...9056
                <svg xmlns="http://www.w3.org/2000/svg" width="18px" fill="none" viewBox="0 0 24 24"
                  stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                    d="M7 21h10a2 2 0 002-2V9.414a1 1 0 00-.293-.707l-5.414-5.414A1 1 0 0012.586 3H7a2 2 0 00-2 2v14a2 2 0 002 2z" />
                </svg>
              </h6>
              <div class="mt-2">
                <b>A good boy with a bed reputation</b>
              </div>
              <div class="mt-0">
                <p>
                  createing arts,game,photos for NFT platforms. folllow me and
                  stay in trend
                </p>
              </div>
              <div>
                <ul class="d-flex ms-4 list-inline justify-content-center">
                  <li class="pe-3">
                    <a href="#"><b-img :src="require('@/assets/images/icon/08.png')" class="img-fluid rounded"
                        alt="facebook" loading="lazy" /></a>
                  </li>
                  <li class="pe-3">
                    <a href="#"><b-img :src="require('@/assets/images/icon/09.png')" class="img-fluid rounded"
                        alt="Twitter" loading="lazy" /></a>
                  </li>
                  <li class="pe-3">
                    <a href="#"><b-img :src="require('@/assets/images/icon/10.png')" class="img-fluid rounded"
                        alt="Instagram" loading="lazy" /></a>
                  </li>
                  <li class="pe-3">
                    <a href="#"><b-img :src="require('@/assets/images/icon/13.png')" class="img-fluid rounded"
                        alt="linkedin" loading="lazy" /></a>
                  </li>
                </ul>
              </div>
              <div class="d-flex d-flex justify-content-between align-items-center">
                <h6>Following:</h6>
                <p class="mb-0">346</p>
              </div>
              <div class="d-flex d-flex justify-content-between">
                <h6>Followers:</h6>
                <p class="mb-0">346</p>
              </div>
              <button type="button" class="btn btn-primary rounded-pill w-100 mt-3">
                folllow
              </button>
            </div>
          </b-card>
        </b-col>
        <div class="col-lg-8">
          <div class="card cardnavbar">
            <div class="user-tabing">
              <ul
                class="nav nav-pills d-flex align-items-center justify-content-center profile-feed-items p-0 m-0 round">
                <li class="nav-item col-12 col-sm-2 p-0">
                  <a class="nav-link active" href="#pills-sale-tab" data-bs-toggle="pill"
                    data-bs-target="#pills-sale-tab" role="button">On sale</a>
                </li>
                <li class="nav-item col-12 col-sm-3 p-0">
                  <a class="nav-link" href="#pills-collection-tab" data-bs-toggle="pill"
                    data-bs-target="#pills-collection-tab" role="button">Collectibles</a>
                </li>
                <li class="nav-item col-12 col-sm-2 p-0">
                  <a class="nav-link" href="#pills-created-tab" data-bs-toggle="pill"
                    data-bs-target="#pills-created-tab" role="button">Created</a>
                </li>
                <li class="nav-item col-12 col-sm-2 p-0">
                  <a class="nav-link" href="#pills-liked-tab" data-bs-toggle="pill" data-bs-target="#pills-liked-tab"
                    role="button">Liked</a>
                </li>
                <li class="nav-item col-12 col-sm-3 p-0">
                  <a class="nav-link" href="#pills-activity-tab" data-bs-toggle="pill"
                    data-bs-target="#pills-activity-tab" role="button">Activity</a>
                </li>
              </ul>
            </div>
          </div>
          <div class="tab-content forum-content">
            <!-- on sale tab-->
            <div class="tab-pane fade show active" id="pills-sale-tab">
              <div class="row">
                <div class="col-sm-4" v-for="(card, index) in cards" :key="index">
                  <div class="card">
                    <div class="card-body">
                      <div class="event-images position-relative">
                        <a>
                          <img :src="card.image" class="img-fluid rounded" alt="Responsive image" loading="lazy" />
                        </a>
                      </div>
                      <span class="badge bg-danger image-offer-btn">{{
                card.discount
              }}</span>
                      <div class="mt-3">
                        <h5>{{ card.title }}</h5>
                      </div>
                      <div class="mt-1">
                        <small><small class="text-primary">{{ card.price }}</small>
                          1 of {{ card.total }}</small>
                      </div>
                      <div class="mt-0">
                        <small>Highest bid:<small class="text-primary ms-1">{{
                card.highestBid
              }}</small></small>
                      </div>
                      <hr class="hr-horizontal" />
                      <div class="d-flex justify-content-between">
                        <div>
                          <p class="mb-0">
                            <svg xmlns="http://www.w3.org/2000/svg" width="16px" class="mb-0" fill="none"
                              viewBox="0 0 24 24" stroke="currentColor">
                              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
                            </svg>
                            {{ card.time }}
                            <small class="ms-1">{{ card.timeAgo }}</small>
                          </p>
                        </div>
                        <p class="mb-0">
                          <svg xmlns="http://www.w3.org/2000/svg" width="16px" fill="none" viewBox="0 0 24 24"
                            stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                              d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z" />
                          </svg>
                          {{ card.likes }}
                          <small class="ms-1">{{ card.likesCount }}</small>
                        </p>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
              <!-- collectibles tab-->
            </div>
            <div class="tab-pane fade" id="pills-collection-tab">
              <div class="row">
                <div class="col-sm-4" v-for="(card, index) in collectibles" :key="index">
                  <div class="card">
                    <div class="card-body">
                      <div class="event-images position-relative">
                        <a>
                          <img :src="card.image" class="img-fluid rounded" alt="Responsive image" loading="lazy" />
                        </a>
                      </div>
                      <span class="badge bg-danger image-offer-btn">{{
                card.discount
              }}</span>
                      <div class="mt-3">
                        <h5>{{ card.title }}</h5>
                      </div>
                      <div class="mt-1">
                        <small><small class="text-primary">{{ card.price }}</small>
                          1 of {{ card.total }}</small>
                      </div>
                      <div class="mt-0">
                        <small>Highest bid:<small class="text-primary ms-1">{{
                card.highestBid
              }}</small></small>
                      </div>
                      <hr class="hr-horizontal" />
                      <div class="d-flex justify-content-between">
                        <div>
                          <p class="mb-0">
                            <svg xmlns="http://www.w3.org/2000/svg" width="16px" class="mb-0" fill="none"
                              viewBox="0 0 24 24" stroke="currentColor">
                              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
                            </svg>
                            {{ card.time }}
                            <small class="ms-1">{{ card.timeAgo }}</small>
                          </p>
                        </div>
                        <p class="mb-0">
                          <svg xmlns="http://www.w3.org/2000/svg" width="16px" fill="none" viewBox="0 0 24 24"
                            stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                              d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z" />
                          </svg>
                          {{ card.likes }}
                          <small class="ms-1">{{ card.likesCount }}</small>
                        </p>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>

            <!-- created tab-->
            <div class="tab-pane fade" id="pills-created-tab">
              <div class="card">
                <div class="card-header d-flex justify-content-between">
                  <div class="header-title">
                    <h4 class="card-title">your comments</h4>
                  </div>
                </div>
                <div class="card-body">
                  <div class="align-items-center d-flex borderbox1 flex-wrap">
                    <img src="@/assets/images/user/02.jpg" alt="userimg" class="avatar-40 rounded-circle" />
                    <h6 class="ms-2">Theodocre</h6>
                    <a class="ms-3" href="#">@john_ram</a>
                    <div class="ms-auto d-flex">
                      <svg xmlns="http://www.w3.org/2000/svg" width="16px" viewBox="0 0 20 20" fill="currentColor">
                        <path fill-rule="evenodd"
                          d="M10 18a8 8 0 100-16 8 8 0 000 16zm1-12a1 1 0 10-2 0v4a1 1 0 00.293.707l2.828 2.829a1 1 0 101.415-1.415L11 9.586V6z"
                          clip-rule="evenodd"></path>
                      </svg>
                      <span class="mx-1"><small>35 mins</small></span>
                    </div>
                  </div>
                  <p>
                    In any moment of decsion, the best thing of you can do
                    thing,the next best thing is the wrong thing,and the worst
                    thing of
                  </p>
                  <div class="align-items-center d-flex borderbox1 flex-wrap">
                    <img src="@/assets/images/user/03.jpg" alt="userimg" class="avatar-40 rounded-circle" />
                    <h6 class="ms-2">Theodocre</h6>
                    <a class="ms-3" href="#">@john_ram</a>
                    <div class="ms-auto d-flex">
                      <svg xmlns="http://www.w3.org/2000/svg" width="16px" viewBox="0 0 20 20" fill="currentColor">
                        <path fill-rule="evenodd"
                          d="M10 18a8 8 0 100-16 8 8 0 000 16zm1-12a1 1 0 10-2 0v4a1 1 0 00.293.707l2.828 2.829a1 1 0 101.415-1.415L11 9.586V6z"
                          clip-rule="evenodd"></path>
                      </svg>
                      <span class="mx-1"><small>15 mins</small></span>
                    </div>
                  </div>
                  <p>great pictures!!</p>
                  <div class="align-items-center d-flex borderbox1 flex-wrap">
                    <img src="@/assets/images/user/02.jpg" alt="userimg" class="avatar-40 rounded-circle" />
                    <h6 class="ms-2">Theodocre</h6>
                    <a class="ms-3" href="#">@john_ram</a>
                    <div class="ms-auto d-flex">
                      <svg xmlns="http://www.w3.org/2000/svg" width="16px" viewBox="0 0 20 20" fill="currentColor">
                        <path fill-rule="evenodd"
                          d="M10 18a8 8 0 100-16 8 8 0 000 16zm1-12a1 1 0 10-2 0v4a1 1 0 00.293.707l2.828 2.829a1 1 0 101.415-1.415L11 9.586V6z"
                          clip-rule="evenodd"></path>
                      </svg>
                      <span class="mx-1"><small>35 mins</small></span>
                    </div>
                  </div>
                  <p>
                    In any moment of decsion, the best thing of you can do
                    thing,the next best thing is the wrong thing,and the worst
                    thing of
                  </p>
                  <div class="align-items-center d-flex borderbox1 flex-wrap">
                    <img src="@/assets/images/user/03.jpg" alt="userimg" class="avatar-40 rounded-circle" />
                    <h6 class="ms-2">Theodocre</h6>
                    <a class="ms-3" href="#">@john_ram</a>
                    <div class="ms-auto d-flex">
                      <svg xmlns="http://www.w3.org/2000/svg" width="16px" viewBox="0 0 20 20" fill="currentColor">
                        <path fill-rule="evenodd"
                          d="M10 18a8 8 0 100-16 8 8 0 000 16zm1-12a1 1 0 10-2 0v4a1 1 0 00.293.707l2.828 2.829a1 1 0 101.415-1.415L11 9.586V6z"
                          clip-rule="evenodd"></path>
                      </svg>
                      <span class="mx-1"><small>15 mins</small></span>
                    </div>
                  </div>
                  <p>great pictures!!</p>
                  <div class="align-items-center d-flex borderbox1 flex-wrap">
                    <img src="@/assets/images/user/02.jpg" alt="userimg" class="avatar-40 rounded-circle" />
                    <h6 class="ms-2">Theodocre</h6>
                    <a class="ms-3" href="#">@john_ram</a>
                    <div class="ms-auto d-flex">
                      <svg xmlns="http://www.w3.org/2000/svg" width="16px" viewBox="0 0 20 20" fill="currentColor">
                        <path fill-rule="evenodd"
                          d="M10 18a8 8 0 100-16 8 8 0 000 16zm1-12a1 1 0 10-2 0v4a1 1 0 00.293.707l2.828 2.829a1 1 0 101.415-1.415L11 9.586V6z"
                          clip-rule="evenodd"></path>
                      </svg>
                      <span class="mx-1"><small>35 mins</small></span>
                    </div>
                  </div>
                  <p>
                    In any moment of decsion, the best thing of you can do
                    thing,the next best thing is the wrong thing,and the worst
                    thing of
                  </p>
                  <div class="align-items-center d-flex borderbox1 flex-wrap">
                    <img src="@/assets/images/user/03.jpg" alt="userimg" class="avatar-40 rounded-circle" />
                    <h6 class="ms-2">Theodocre</h6>
                    <a class="ms-3" href="#">@john_ram</a>
                    <div class="ms-auto d-flex">
                      <svg xmlns="http://www.w3.org/2000/svg" width="16px" viewBox="0 0 20 20" fill="currentColor">
                        <path fill-rule="evenodd"
                          d="M10 18a8 8 0 100-16 8 8 0 000 16zm1-12a1 1 0 10-2 0v4a1 1 0 00.293.707l2.828 2.829a1 1 0 101.415-1.415L11 9.586V6z"
                          clip-rule="evenodd"></path>
                      </svg>
                      <span class="mx-1"><small>15 mins</small></span>
                    </div>
                  </div>
                  <p>great pictures!!</p>
                  <div class="align-items-center d-flex borderbox1 flex-wrap">
                    <img src="@/assets/images/user/02.jpg" alt="userimg" class="avatar-40 rounded-circle" />
                    <h6 class="ms-2">Theodocre</h6>
                    <a class="ms-3" href="#">@john_ram</a>
                    <div class="ms-auto d-flex">
                      <svg xmlns="http://www.w3.org/2000/svg" width="16px" viewBox="0 0 20 20" fill="currentColor">
                        <path fill-rule="evenodd"
                          d="M10 18a8 8 0 100-16 8 8 0 000 16zm1-12a1 1 0 10-2 0v4a1 1 0 00.293.707l2.828 2.829a1 1 0 101.415-1.415L11 9.586V6z"
                          clip-rule="evenodd"></path>
                      </svg>
                      <span class="mx-1"><small>35 mins</small></span>
                    </div>
                  </div>
                  <p>
                    In any moment of decsion, the best thing of you can do
                    thing,the next best thing is the wrong thing,and the worst
                    thing of
                  </p>
                  <div class="align-items-center d-flex borderbox1 flex-wrap">
                    <img src="@/assets/images/user/03.jpg" alt="userimg" class="avatar-40 rounded-circle" />
                    <h6 class="ms-2">Theodocre</h6>
                    <a class="ms-3" href="#">@john_ram</a>
                    <div class="ms-auto d-flex">
                      <svg xmlns="http://www.w3.org/2000/svg" width="16px" viewBox="0 0 20 20" fill="currentColor">
                        <path fill-rule="evenodd"
                          d="M10 18a8 8 0 100-16 8 8 0 000 16zm1-12a1 1 0 10-2 0v4a1 1 0 00.293.707l2.828 2.829a1 1 0 101.415-1.415L11 9.586V6z"
                          clip-rule="evenodd"></path>
                      </svg>
                      <span class="mx-1"><small>15 mins</small></span>
                    </div>
                  </div>
                  <p>great pictures!!</p>
                </div>
              </div>
            </div>

            <!-- liked tab-->
            <div class="tab-pane fade" id="pills-liked-tab">
              <div class="row">
                <div class="col-sm-4" v-for="(card, index) in liked" :key="index">
                  <div class="card">
                    <div class="card-body">
                      <div class="event-images position-relative">
                        <a :href="card.image" data-fslightbox="gallery">
                          <img :src="card.image" class="img-fluid rounded" alt="Responsive image" loading="lazy" />
                        </a>
                      </div>
                      <hr class="hr-horizontal" />
                      <div class="d-flex justify-content-between">
                        <div class="mb-0">
                          <svg xmlns="http://www.w3.org/2000/svg" width="16px" class="mb-0" fill="none"
                            viewBox="0 0 24 24" stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                              d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
                          </svg>{{ "" }}
                          <small class="ms-1">{{ card.time }}</small>
                        </div>
                        <div class="mb-0">
                          <svg xmlns="http://www.w3.org/2000/svg" width="16px" class="h-5 w-5" viewBox="0 0 20 20"
                            fill="currentColor">
                            <path fill-rule="evenodd"
                              d="M3.172 5.172a4 4 0 015.656 0L10 6.343l1.172-1.171a4 4 0 115.656 5.656L10 17.657l-6.828-6.829a4 4 0 010-5.656z"
                              clip-rule="evenodd" />
                          </svg>{{ "" }}
                          <small class="ms-1">{{ card.likes }}</small>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
              <div class="row">
                <div class="col-sm-4" v-for="(card, index) in liked2" :key="index">
                  <div class="card">
                    <div class="card-body">
                      <div class="event-images position-relative">
                        <a>
                          <img :src="card.image" class="img-fluid rounded" alt="Responsive image" loading="lazy" />
                        </a>
                      </div>
                      <span class="badge bg-danger image-offer-btn">{{
                card.discount
              }}</span>
                      <div class="mt-3">
                        <h5>{{ card.title }}</h5>
                      </div>
                      <div class="mt-1">
                        <small><small class="text-primary">{{ card.price }}</small>
                          1 of {{ card.total }}</small>
                      </div>
                      <div class="mt-0">
                        <small>Highest bid:<small class="text-primary ms-1">{{
                card.highestBid
              }}</small></small>
                      </div>
                      <hr class="hr-horizontal" />
                      <div class="d-flex justify-content-between">
                        <div>
                          <p class="mb-0">
                            <svg xmlns="http://www.w3.org/2000/svg" width="16px" class="mb-0" fill="none"
                              viewBox="0 0 24 24" stroke="currentColor">
                              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
                            </svg>
                            {{ card.time }}
                            <small class="ms-1">{{ card.timeAgo }}</small>
                          </p>
                        </div>
                        <p class="mb-0">
                          <svg xmlns="http://www.w3.org/2000/svg" width="16px" fill="none" viewBox="0 0 24 24"
                            stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                              d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z" />
                          </svg>
                          {{ card.likes }}
                          <small class="ms-1">{{ card.likesCount }}</small>
                        </p>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>

            <!-- activity tab-->
            <div class="tab-pane fade" id="pills-activity-tab">
              <div class="row">
                <div class="col-sm-4" v-for="(card, index) in activity" :key="index">
                  <div class="card">
                    <div class="card-body">
                      <div class="event-images position-relative">
                        <a>
                          <img :src="card.image" class="img-fluid rounded" alt="Responsive image" loading="lazy" />
                        </a>
                      </div>
                      <span class="badge bg-danger image-offer-btn">{{
                card.discount
              }}</span>
                      <div class="mt-3">
                        <h5>{{ card.title }}</h5>
                      </div>
                      <div class="mt-1">
                        <small><small class="text-primary">{{ card.price }}</small>
                          1 of {{ card.total }}</small>
                      </div>
                      <div class="mt-0">
                        <small>Highest bid:<small class="text-primary ms-1">{{
                card.highestBid
              }}</small></small>
                      </div>
                      <hr class="hr-horizontal" />
                      <div class="d-flex justify-content-between">
                        <div>
                          <p class="mb-0">
                            <svg xmlns="http://www.w3.org/2000/svg" width="16px" class="mb-0" fill="none"
                              viewBox="0 0 24 24" stroke="currentColor">
                              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
                            </svg>
                            {{ card.time }}
                            <small class="ms-1">{{ card.timeAgo }}</small>
                          </p>
                        </div>
                        <p class="mb-0">
                          <svg xmlns="http://www.w3.org/2000/svg" width="16px" fill="none" viewBox="0 0 24 24"
                            stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                              d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z" />
                          </svg>
                          {{ card.likes }}
                          <small class="ms-1">{{ card.likesCount }}</small>
                        </p>
                      </div>
                    </div>
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
  data() {
    return {
      name: "market1",
      cards: [
        {
          image: require("@/assets/images/page-img/51.jpg"),
          discount: "40% off",
          title: "Fragments",
          price: "0.080 ETH",
          total: 56,
          highestBid: "0.080 ETH",
          time: "",
          timeAgo: "8 hours ago",
          likes: "",
          likesCount: "36",
        },
        {
          image: require("@/assets/images/page-img/52.jpg"),
          discount: "80% off",
          title: "Shine brights_00",
          price: "0.003 ETH",
          total: 2,
          highestBid: "0.004 ETH",
          time: "",
          timeAgo: "8 hours ago",
          likes: "",
          likesCount: "36",
        },
        {
          image: require("@/assets/images/page-img/53.jpg"),
          discount: "30% off",
          title: "Anonimoic face",
          price: "0.034 ETH",
          total: 56,
          highestBid: "0.045 ETH",
          time: "",
          timeAgo: "8 days ago",
          likes: "",
          likesCount: "1k",
        },
        {
          image: require("@/assets/images/page-img/54.jpg"),
          discount: "70% off",
          title: "Fire Magic",
          price: "0.009 ETH",
          total: 1,
          highestBid: "0.012 ETH",
          time: "",
          timeAgo: "12 hours ago",
          likes: "",
          likesCount: "786",
        },
        {
          image: require("@/assets/images/page-img/55.jpg"),
          discount: "50% off",
          title: "Smileface",
          price: "0.045 ETH",
          total: 1,
          highestBid: "0.048 ETH",
          time: "",
          timeAgo: "1 days ago",
          likes: "",
          likesCount: "3k",
        },
      ],
      collectibles: [
        {
          image: require("@/assets/images/page-img/56.jpg"),
          title: "Fragments",
          price: "0.080 ETH",
          total: 56,
          highestBid: "0.080 ETH",
          time: "",
          timeAgo: "6 hours ago",
          likes: "",
          likesCount: "674",
        },
        {
          image: require("@/assets/images/page-img/57.jpg"),
          title: "Shine Brights_00",
          price: "0.003 ETH",
          total: 2,
          highestBid: "0.004 ETH",
          time: "",
          timeAgo: "8 hours ago",
          likes: "",
          likesCount: "36",
        },
        {
          image: require("@/assets/images/page-img/58.jpg"),
          title: "Anonimoic Face",
          price: "0.034 ETH",
          total: 56,
          highestBid: "0.045 ETH",
          time: "",
          timeAgo: "8 days ago",
          likes: "",
          likesCount: "1k",
        },
        {
          image: require("@/assets/images/page-img/59.jpg"),
          title: "Fire Magic",
          price: "0.009 ETH",
          total: 1,
          highestBid: "0.012ETH",
          time: "",
          timeAgo: "12 hours ago",
          likes: "",
          likesCount: "786",
        },
        {
          image: require("@/assets/images/page-img/60.jpg"),
          title: "Edition _02",
          price: "0.002 ETH",
          total: 6,
          highestBid: "0.080 ETH",
          time: "",
          timeAgo: "12 hours ago",
          likes: "",
          likesCount: "45",
        },
        {
          image: require("@/assets/images/page-img/61.jpg"),
          title: "Smileface",
          price: "0.045 ETH",
          total: 1,
          highestBid: "0.048 ETH",
          time: "",
          timeAgo: "1 days ago",
          likes: "",
          likesCount: "3k",
        },
      ],
      liked: [
        {
          image: require("@/assets/images/page-img/62.jpg"),
          time: "6 hours ago",
          likes: "674",
        },
        {
          image: require("@/assets/images/page-img/59.jpg"),
          time: "6 hours ago",
          likes: "674",
        },
        {
          image: require("@/assets/images/page-img/55.jpg"),
          time: "6 hours ago",
          likes: "674",
        },
      ],
      liked2: [
        {
          image: require("@/assets/images/page-img/59.jpg"),
          title: "Fire Magic",
          price: "0.009 ETH",
          total: 1,
          highestBid: "0.012ETH",
          time: "",
          timeAgo: "12 hours ago",
          likes: "",
          likesCount: "786",
        },
        {
          image: require("@/assets/images/page-img/60.jpg"),
          title: "Edition _02",
          price: "0.002 ETH",
          total: 6,
          highestBid: "0.080 ETH",
          time: "",
          timeAgo: "12 hours ago",
          likes: "",
          likesCount: "45",
        },
        {
          image: require("@/assets/images/page-img/61.jpg"),
          title: "Smileface",
          price: "0.045 ETH",
          total: 1,
          highestBid: "0.048 ETH",
          time: "",
          timeAgo: "1 days ago",
          likes: "",
          likesCount: "3k",
        },
      ],
      activity: [
        {
          image: require("@/assets/images/page-img/51.jpg"),
          title: "Fragments",
          price: "0.080 ETH",
          total: 56,
          highestBid: "0.080 ETH",
          time: "",
          timeAgo: "6 hours ago",
          likes: "",
          likesCount: "674",
        },
        {
          image: require("@/assets/images/page-img/59.jpg"),
          title: "Shine Brights_00",
          price: "0.003 ETH",
          total: 2,
          highestBid: "0.004 ETH",
          time: "",
          timeAgo: "8 hours ago",
          likes: "",
          likesCount: "36",
        },
        {
          image: require("@/assets/images/page-img/64.jpg"),
          title: "Anonimoic Face",
          price: "0.034 ETH",
          total: 56,
          highestBid: "0.045 ETH",
          time: "",
          timeAgo: "8 days ago",
          likes: "",
          likesCount: "1k",
        },
        {
          image: require("@/assets/images/page-img/59.jpg"),
          title: "Fire Magic",
          price: "0.009 ETH",
          total: 1,
          highestBid: "0.012ETH",
          time: "",
          timeAgo: "12 hours ago",
          likes: "",
          likesCount: "786",
        },
        {
          image: require("@/assets/images/page-img/60.jpg"),
          title: "Edition _02",
          price: "0.002 ETH",
          total: 6,
          highestBid: "0.080 ETH",
          time: "",
          timeAgo: "12 hours ago",
          likes: "",
          likesCount: "45",
        },
        {
          image: require("@/assets/images/page-img/61.jpg"),
          title: "Smileface",
          price: "0.045 ETH",
          total: 1,
          highestBid: "0.048 ETH",
          time: "",
          timeAgo: "1 days ago",
          likes: "",
          likesCount: "3k",
        },
      ],
    };
  },
};
</script>
