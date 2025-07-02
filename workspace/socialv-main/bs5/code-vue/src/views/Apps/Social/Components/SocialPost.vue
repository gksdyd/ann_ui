<template>
  <b-col sm="12" class="social-post">
    <b-card no-body class="card-block card-stretch card-height">
      <b-card-body>
        <div class="user-post-data">
          <div class="d-flex align-items-center justify-content-between">
            <div class="me-3 flex-shrik-0">
              <img class="border border-2 rounded-circle user-post-profile" src="@/assets/images/user/01.jpg" alt="" />
            </div>
            <div class="w-100">
              <div class="d-flex align-items-center justify-content-between">
                <div class="">
                  <h6 class="mb-0 d-inline-block">Anna Sthesia</h6>{{ "" }}
                  <span class="d-inline-block text-primary">
                    <svg class="align-text-bottom" width="17" height="17" viewBox="0 0 17 17" fill="none"
                      xmlns="http://www.w3.org/2000/svg">
                      <path fill-rule="evenodd" clip-rule="evenodd"
                        d="M11.8457 0H4.34822C1.73547 0 0.0974121 1.84995 0.0974121 4.46789V11.5321C0.0974121 14.1501 1.72768 16 4.34822 16H11.8449C14.4663 16 16.0974 14.1501 16.0974 11.5321V4.46789C16.0974 1.84995 14.4663 0 11.8457 0Z"
                        fill="currentColor" />
                      <path d="M5.09741 7.99978L7.09797 9.9995L11.0974 6.00006" stroke="white" stroke-width="1.5"
                        stroke-linecap="round" stroke-linejoin="round" />
                    </svg>
                  </span>{{ "" }}
                  <span class="mb-0 d-inline-block text-capitalize fw-medium">posted an update</span>
                  <p class="mb-0">2 minutes ago</p>
                </div>
                <div class="card-post-toolbar">
                  <div class="dropdown">
                    <span class="dropdown-toggle material-symbols-outlined" data-bs-toggle="dropdown"
                      aria-haspopup="true" aria-expanded="false" role="button">
                      more_horiz
                    </span>
                    <div class="dropdown-menu m-0 p-0">
                      <a class="dropdown-item p-3" href="#">
                        <div class="d-flex align-items-top">
                          <span class="material-symbols-outlined"> save </span>
                          <div class="data ms-2">
                            <h6>Save Post</h6>
                            <p class="mb-0">Add this to your saved items</p>
                          </div>
                        </div>
                      </a>
                      <a class="dropdown-item p-3" href="#">
                        <div class="d-flex align-items-top">
                          <span class="material-symbols-outlined">
                            cancel
                          </span>
                          <div class="data ms-2">
                            <h6>Hide Post</h6>
                            <p class="mb-0">See fewer posts like this.</p>
                          </div>
                        </div>
                      </a>
                      <a class="dropdown-item p-3" href="#">
                        <div class="d-flex align-items-top">
                          <span class="material-symbols-outlined">
                            person_remove
                          </span>
                          <div class="data ms-2">
                            <h6>Unfollow User</h6>
                            <p class="mb-0">
                              Stop seeing posts but stay friends.
                            </p>
                          </div>
                        </div>
                      </a>

                      <a class="dropdown-item p-3" href="#">
                        <div class="d-flex align-items-top">
                          <span class="material-symbols-outlined">
                            notifications
                          </span>
                          <div class="data ms-2">
                            <h6>Notifications</h6>
                            <p class="mb-0">
                              Turn on notifications for this post
                            </p>
                          </div>
                        </div>
                      </a>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="mt-4">
          <p class="m-0">
            "Energy, the tangible expression of pure thought, propels intentions
            into powerful actions, bridging the gap between mind and
            manifestation."
          </p>
          <ul class="list-inline m-0 p-0 d-flex flex-wrap gap-1">
            <li>
              <a href="#">#friends</a>
            </li>
            <li>
              <a href="#">#party</a>
            </li>
            <li>
              <a href="#">#birthday</a>
            </li>
            <li>
              <a href="#">#together</a>
            </li>
            <li>
              <a href="#">#celebration</a>
            </li>
          </ul>
        </div>
        <div class="user-post mt-4">
          <a class="rounded" data-fslightbox="gallery" @click="toggler = !toggler">
            <img src="@/assets/images/page-img/fun.jpg" alt="post-image" class="img-fluid rounded w-100"
              loading="lazy" />
          </a>
        </div>
        <div class="post-meta-likes mt-4">
          <div class="d-flex align-items-center gap-2 flex-wrap">
            <ul class="list-inline m-0 p-0 post-user-liked-list">
              <li>
                <img src="@/assets/images/user/01.jpg" alt="userimg" class="rounded-circle img-fluid userimg"
                  loading="lazy" />
              </li>
              {{
                ""
              }}
              <li>
                <img src="@/assets/images/user/02.jpg" alt="userimg" class="rounded-circle img-fluid userimg"
                  loading="lazy" />
              </li>
              {{
                ""
              }}
              <li>
                <img src="@/assets/images/user/03.jpg" alt="userimg" class="rounded-circle img-fluid userimg"
                  loading="lazy" />
              </li>
              {{
                ""
              }}
              <li>
                <img src="@/assets/images/user/04.jpg" alt="userimg" class="rounded-circle img-fluid userimg"
                  loading="lazy" />
              </li>
            </ul>
            <div class="d-inline-flex align-items-center gap-1">
              <h6 class="m-0 font-size-14">Aliana Molex</h6>
              <span class="text-capitalize font-size-14 fw-medium" type="button" data-bs-toggle="modal"
                data-bs-target="#likemodal">and 208 others liked this</span>
            </div>
          </div>
        </div>

        <div class="comment-area mt-4 pt-4 border-top">
          <div class="d-flex justify-content-between align-items-center flex-wrap">
            <div class="like-block position-relative d-flex align-items-center flex-shrink-0">
              <div class="like-data">
                <div class="dropdown">
                  <span class="dropdown-toggle" data-bs-toggle="dropdown" aria-haspopup="true" aria-expanded="false"
                    role="button">
                    <span class="material-symbols-outlined align-text-top font-size-20">
                      thumb_up
                    </span>{{ "" }}
                    <span class="fw-medium">140 Likes</span>
                  </span>
                  <div class="dropdown-menu py-2 shadow">
                    <a class="ms-2 me-2" href="#" v-b-tooltip.hover title="Like"><img src="@/assets/images/icon/01.png"
                        class="img-fluid" alt="like" loading="lazy" /></a>
                    <a class="me-2" href="#" v-b-tooltip.hover title="Love"><img src="@/assets/images/icon/02.png"
                        class="img-fluid" alt="love" loading="lazy" /></a>
                    <a class="me-2" href="#" v-b-tooltip.hover title="Happy"><img src="@/assets/images/icon/03.png"
                        class="img-fluid" alt="happy" loading="lazy" /></a>
                    <a class="me-2" href="#" v-b-tooltip.hover title="HaHa"><img src="@/assets/images/icon/04.png"
                        class="img-fluid" alt="haha" loading="lazy" /></a>
                    <a class="me-2" href="#" v-b-tooltip.hover title="Think"><img src="@/assets/images/icon/05.png"
                        class="img-fluid" alt="think" loading="lazy" /></a>
                    <a class="me-2" href="#" v-b-tooltip.hover title="Sad"><img src="@/assets/images/icon/06.png"
                        class="img-fluid" alt="sad" loading="lazy" /></a>
                    <a class="me-2" href="#" v-b-tooltip.hover title="Lovely"><img src="@/assets/images/icon/07.png"
                        class="img-fluid" alt="lovely" loading="lazy" /></a>
                  </div>
                </div>
              </div>
            </div>
            <div class="d-flex align-items-center gap-3 flex-shrink-0">
              <div class="total-comment-block" type="button" data-bs-toggle="collapse"
                data-bs-target="#commentcollapes1" aria-expanded="false" aria-controls="commentcollapes">
                <span class="material-symbols-outlined align-text-top font-size-20">
                  comment
                </span>
                {{ "" }}
                <span class="fw-medium">20 Comment</span>
              </div>
              <div class="share-block d-flex align-items-center feather-icon">
                <a href="#" data-bs-toggle="modal" data-bs-target="#modal-share-offcanvas" aria-controls="share-btn"
                  class="d-flex align-items-center">
                  <span class="material-symbols-outlined align-text-top font-size-20">
                    share
                  </span>
                  <span class="ms-1 fw-medium">99 Share</span></a>
                <ShareOffcanvas />
              </div>
            </div>
          </div>
          <div class="collapse mt-4 pt-4 border-top" id="commentcollapes1">
            <ul class="list-inline m-o p-0 comment-list">
              <li class="mb-3">
                <div class="comment-list-block">
                  <div class="d-flex align-items-center gap-3">
                    <div class="comment-list-user-img flex-shrink-0">
                      <img src="@/assets/images/user/13.jpg" alt="userimg" class="avatar-48 rounded-circle img-fluid"
                        loading="lazy" />
                    </div>
                    <div class="comment-list-user-data">
                      <div class="d-inline-flex align-items-center gap-1 flex-wrap">
                        <h6 class="m-0">Bob Frapples</h6>
                        <span class="d-inline-block text-primary">
                          <svg class="align-text-bottom" xmlns="http://www.w3.org/2000/svg" width="17" height="17"
                            viewBox="0 0 17 17" fill="none">
                            <path fill-rule="evenodd" clip-rule="evenodd"
                              d="M12.2483 0.216553H4.75081C2.13805 0.216553 0.5 2.0665 0.5 4.68444V11.7487C0.5 14.3666 2.13027 16.2166 4.75081 16.2166H12.2475C14.8689 16.2166 16.5 14.3666 16.5 11.7487V4.68444C16.5 2.0665 14.8689 0.216553 12.2483 0.216553Z"
                              fill="currentColor" />
                            <path d="M5.5 8.21627L7.50056 10.216L11.5 6.21655" stroke="white" stroke-width="1.5"
                              stroke-linecap="round" stroke-linejoin="round" />
                          </svg>
                        </span>
                        <spna class="fw-medium small text-capitalize">3 min ago</spna>
                      </div>
                    </div>
                  </div>
                  <div class="comment-list-user-comment">
                    <div class="comment-list-comment">
                      "Just stumbled upon this post and it's giving me all the
                      feels! 🙌"
                    </div>
                    <div class="comment-list-action mt-2">
                      <ul class="list-inline m-0 p-0 d-flex align-items-center gap-2">
                        <li>
                          <div class="like-block position-relative d-flex align-items-center flex-shrink-0">
                            <div class="like-data">
                              <div class="dropdown">
                                <span class="dropdown-toggle" data-bs-toggle="dropdown" aria-haspopup="true"
                                  aria-expanded="false" role="button">
                                  <span class="material-symbols-outlined align-text-top font-size-18">
                                    thumb_up
                                  </span>
                                  {{ "" }}
                                  <span class="fw-medium small">Likes</span>
                                </span>
                                <div class="dropdown-menu py-2 shadow">
                                  <a class="ms-2 me-2" href="#" data-bs-toggle="tooltip" data-bs-placement="top"
                                    title="Like"><img src="@/assets/images/icon/01.png" class="img-fluid" alt="like"
                                      loading="lazy" /></a>
                                  <a class="me-2" href="#" data-bs-toggle="tooltip" data-bs-placement="top"
                                    title="Love"><img src="@/assets/images/icon/02.png" class="img-fluid" alt="love"
                                      loading="lazy" /></a>
                                  <a class="me-2" href="#" data-bs-toggle="tooltip" data-bs-placement="top"
                                    title="Happy"><img src="@/assets/images/icon/03.png" class="img-fluid" alt="happy"
                                      loading="lazy" /></a>
                                  <a class="me-2" href="#" data-bs-toggle="tooltip" data-bs-placement="top"
                                    title="HaHa"><img src="@/assets/images/icon/04.png" class="img-fluid" alt="haha"
                                      loading="lazy" /></a>
                                  <a class="me-2" href="#" data-bs-toggle="tooltip" data-bs-placement="top"
                                    title="Think"><img src="@/assets/images/icon/05.png" class="img-fluid" alt="think"
                                      loading="lazy" /></a>
                                  <a class="me-2" href="#" data-bs-toggle="tooltip" data-bs-placement="top"
                                    title="Sad"><img src="@/assets/images/icon/06.png" class="img-fluid" alt="sad"
                                      loading="lazy" /></a>
                                  <a class="me-2" href="#" data-bs-toggle="tooltip" data-bs-placement="top"
                                    title="Lovely"><img src="@/assets/images/icon/07.png" class="img-fluid" alt="lovely"
                                      loading="lazy" /></a>
                                </div>
                              </div>
                            </div>
                          </div>
                        </li>
                        <li>
                          <span class="fw-medium small" data-bs-toggle="collapse" data-bs-target="#subcomment-collapse1"
                            role="button" aria-expanded="false" aria-controls="collapseExample">
                            Reply
                          </span>
                        </li>
                      </ul>
                      <div class="add-comment-form-block collapse mt-3" id="subcomment-collapse1">
                        <div class="d-flex align-items-center gap-3">
                          <div class="flex-shrink-0">
                            <img src="@/assets/images/user/1.jpg" alt="userimg"
                              class="avatar-48 rounded-circle img-fluid" loading="lazy" />
                          </div>
                          <div class="add-comment-form">
                            <form>
                              <input type="text" class="form-control" placeholder="Write a Comment..." />
                              <button type="submit" class="btn btn-primary font-size-12 text-capitalize px-5">
                                post
                              </button>
                            </form>
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </li>
            </ul>
            <div class="add-comment-form-block">
              <div class="d-flex align-items-center gap-3">
                <div class="flex-shrink-0">
                  <img src="@/assets/images/user/1.jpg" alt="userimg" class="avatar-48 rounded-circle img-fluid"
                    loading="lazy" />
                </div>
                <div class="add-comment-form">
                  <form>
                    <input type="text" class="form-control" placeholder="Write a Comment..." />
                    <button type="submit" class="btn btn-primary font-size-12 text-capitalize px-5">
                      post
                    </button>
                  </form>
                </div>
              </div>
            </div>
          </div>
        </div>
      </b-card-body>
    </b-card>
  </b-col>
  <b-col sm="12" class="social-post">
    <b-card no-body class="card-block card-stretch card-height">
      <b-card-body>
        <div class="user-post-data">
          <div class="d-flex align-items-center justify-content-between">
            <div class="me-3 flex-shrik-0">
              <img class="border border-2 rounded-circle user-post-profile" src="@/assets/images/user/03.jpg" alt="" />
            </div>
            <div class="w-100">
              <div class="d-flex align-items-center justify-content-between">
                <div class="">
                  <h6 class="mb-0 d-inline-block">Barb Ackue</h6>
                  {{ "" }}
                  <span class="d-inline-block text-primary">
                    <svg class="align-text-bottom" width="17" height="17" viewBox="0 0 17 17" fill="none"
                      xmlns="http://www.w3.org/2000/svg">
                      <path fill-rule="evenodd" clip-rule="evenodd"
                        d="M11.8457 0H4.34822C1.73547 0 0.0974121 1.84995 0.0974121 4.46789V11.5321C0.0974121 14.1501 1.72768 16 4.34822 16H11.8449C14.4663 16 16.0974 14.1501 16.0974 11.5321V4.46789C16.0974 1.84995 14.4663 0 11.8457 0Z"
                        fill="currentColor" />
                      <path d="M5.09741 7.99978L7.09797 9.9995L11.0974 6.00006" stroke="white" stroke-width="1.5"
                        stroke-linecap="round" stroke-linejoin="round" />
                    </svg>
                  </span>
                  {{ "" }}
                  <span class="mb-0 d-inline-block text-capitalize fw-medium">Add a New Post</span>
                  <p class="mb-0">1 Hour ago</p>
                </div>
                <div class="card-post-toolbar">
                  <div class="dropdown">
                    <span class="dropdown-toggle material-symbols-outlined" data-bs-toggle="dropdown"
                      aria-haspopup="true" aria-expanded="false" role="button">
                      more_horiz
                    </span>
                    <div class="dropdown-menu m-0 p-0">
                      <a class="dropdown-item p-3" href="#">
                        <div class="d-flex align-items-top">
                          <span class="material-symbols-outlined"> save </span>
                          <div class="data ms-2">
                            <h6>Save Post</h6>
                            <p class="mb-0">Add this to your saved items</p>
                          </div>
                        </div>
                      </a>
                      <a class="dropdown-item p-3" href="#">
                        <div class="d-flex align-items-top">
                          <span class="material-symbols-outlined">
                            cancel
                          </span>
                          <div class="data ms-2">
                            <h6>Hide Post</h6>
                            <p class="mb-0">See fewer posts like this.</p>
                          </div>
                        </div>
                      </a>
                      <a class="dropdown-item p-3" href="#">
                        <div class="d-flex align-items-top">
                          <span class="material-symbols-outlined">
                            person_remove
                          </span>
                          <div class="data ms-2">
                            <h6>Unfollow User</h6>
                            <p class="mb-0">
                              Stop seeing posts but stay friends.
                            </p>
                          </div>
                        </div>
                      </a>

                      <a class="dropdown-item p-3" href="#">
                        <div class="d-flex align-items-top">
                          <span class="material-symbols-outlined">
                            notifications
                          </span>
                          <div class="data ms-2">
                            <h6>Notifications</h6>
                            <p class="mb-0">
                              Turn on notifications for this post
                            </p>
                          </div>
                        </div>
                      </a>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="mt-4">
          <p class="m-0">
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi
            nulla dolor, ornare at commodo non, feugiat non nisi. Phasellus
            faucibus mollis pharetra. Proin blandit ac massa sed rhoncus"
          </p>
          <ul class="list-inline m-0 p-0 d-flex flex-wrap gap-1">
            <li>
              <a href="#">#family</a>
            </li>
            <li>
              <a href="#">#happiness</a>
            </li>
            <li>
              <a href="#">#travelling</a>
            </li>
            <li>
              <a href="#">#camping</a>
            </li>
            <li>
              <a href="#">#climbing</a>
            </li>
          </ul>
        </div>
        <div class="user-post mt-4">
          <b-row class="row">
            <b-col md="4">
              <a data-fslightbox="gallery" @click="toggler = !toggler" href="#" class="rounded">
                <img src="@/assets/images/page-img/boy.jpg" alt="post-image" class="img-fluid rounded w-100"
                  loading="lazy" />
              </a>
            </b-col>
            <b-col md="4" class="mt-md-0 mt-3">
              <a data-fslightbox="gallery" @click="toggler = !toggler" href="#" class="rounded">
                <img src="@/assets/images/page-img/bus.jpg" alt="post-image" class="img-fluid rounded w-100"
                  loading="lazy" />
              </a>
            </b-col>
            <b-col md="4" class="mt-md-0 mt-3">
              <a data-fslightbox="gallery" @click="toggler = !toggler" href="#" class="rounded">
                <img src="@/assets/images/page-img/fd.jpg" alt="post-image" class="img-fluid rounded w-100"
                  loading="lazy" />
              </a>
            </b-col>
          </b-row>
          <b-row class="mt-3">
            <b-col md="6">
              <a data-fslightbox="gallery" @click="toggler = !toggler" href="@/assets/images/page-img/mountain.jpg"
                class="rounded">
                <img src="@/assets/images/page-img/mountain.jpg" alt="post-image" class="img-fluid rounded w-100"
                  loading="lazy" />
              </a>
            </b-col>
            <b-col md="6" class="mt-md-0 mt-3">
              <div class="post-overlay-box h-100 rounded">
                <img src="@/assets/images/page-img/pizza.jpg" alt="post-image"
                  class="img-fluid rounded w-100 h-100 object-cover" loading="lazy" />
                <a data-fslightbox="gallery" @click="toggler = !toggler" href="#" class="rounded font-size-18">+2
                </a>
              </div>
            </b-col>
          </b-row>
        </div>
        <div class="post-meta-likes mt-4">
          <div class="d-flex align-items-center gap-2 flex-wrap">
            <ul class="list-inline m-0 p-0 post-user-liked-list">
              <li>
                <img src="@/assets/images/user/01.jpg" alt="userimg" class="rounded-circle img-fluid userimg"
                  loading="lazy" />
              </li>
              {{
                ""
              }}
              <li>
                <img src="@/assets/images/user/02.jpg" alt="userimg" class="rounded-circle img-fluid userimg"
                  loading="lazy" />
              </li>
              {{
                ""
              }}
              <li>
                <img src="@/assets/images/user/03.jpg" alt="userimg" class="rounded-circle img-fluid userimg"
                  loading="lazy" />
              </li>
              {{
                ""
              }}
              <li>
                <img src="@/assets/images/user/04.jpg" alt="userimg" class="rounded-circle img-fluid userimg"
                  loading="lazy" />
              </li>
            </ul>
            <div class="d-inline-flex align-items-center gap-1">
              <h6 class="m-0 font-size-14">Aliana Molex</h6>
              <span class="text-capitalize font-size-14 fw-medium" type="button" data-bs-toggle="modal"
                data-bs-target="#likemodal">and 208 others liked this</span>
            </div>
          </div>
        </div>
        <div class="comment-area mt-4 pt-4 border-top">
          <div class="d-flex justify-content-between align-items-center flex-wrap">
            <div class="like-block position-relative d-flex align-items-center flex-shrink-0">
              <div class="like-data">
                <div class="dropdown">
                  <span class="dropdown-toggle" data-bs-toggle="dropdown" aria-haspopup="true" aria-expanded="false"
                    role="button">
                    <span class="material-symbols-outlined align-text-top font-size-20">
                      thumb_up
                    </span>{{ "" }}
                    <span class="fw-medium">140 Likes</span>
                  </span>
                  <div class="dropdown-menu py-2 shadow">
                    <a class="ms-2 me-2" href="#" v-b-tooltip.hover title="Like"><img src="@/assets/images/icon/01.png"
                        class="img-fluid" alt="like" loading="lazy" /></a>
                    <a class="me-2" href="#" v-b-tooltip.hover title="Love"><img src="@/assets/images/icon/02.png"
                        class="img-fluid" alt="love" loading="lazy" /></a>
                    <a class="me-2" href="#" v-b-tooltip.hover title="Happy"><img src="@/assets/images/icon/03.png"
                        class="img-fluid" alt="happy" loading="lazy" /></a>
                    <a class="me-2" href="#" v-b-tooltip.hover title="HaHa"><img src="@/assets/images/icon/04.png"
                        class="img-fluid" alt="haha" loading="lazy" /></a>
                    <a class="me-2" href="#" v-b-tooltip.hover title="Think"><img src="@/assets/images/icon/05.png"
                        class="img-fluid" alt="think" loading="lazy" /></a>
                    <a class="me-2" href="#" v-b-tooltip.hover title="Sad"><img src="@/assets/images/icon/06.png"
                        class="img-fluid" alt="sad" loading="lazy" /></a>
                    <a class="me-2" href="#" v-b-tooltip.hover title="Lovely"><img src="@/assets/images/icon/07.png"
                        class="img-fluid" alt="lovely" loading="lazy" /></a>
                  </div>
                </div>
              </div>
            </div>
            <div class="d-flex align-items-center gap-3 flex-shrink-0">
              <div class="total-comment-block" type="button" data-bs-toggle="collapse"
                data-bs-target="#commentcollapes2" aria-expanded="false" aria-controls="commentcollapes2">
                <span class="material-symbols-outlined align-text-top font-size-20">
                  comment
                </span>
                {{ "" }}
                <span class="fw-medium">20 Comment</span>
              </div>
              <div class="share-block d-flex align-items-center feather-icon">
                <a href="#" data-bs-toggle="modal" data-bs-target="#modal-share-offcanvas" aria-controls="share-btn"
                  class="d-flex align-items-center">
                  <span class="material-symbols-outlined align-text-top font-size-20">
                    share
                  </span>
                  <span class="ms-1 fw-medium">99 Share</span></a>
                <ShareOffcanvas />
              </div>
            </div>
          </div>
          <div class="collapse mt-4 pt-4 border-top" id="commentcollapes2">
            <ul class="list-inline m-o p-0 comment-list">
              <li class="mb-3">
                <div class="comment-list-block">
                  <div class="d-flex align-items-center gap-3">
                    <div class="comment-list-user-img flex-shrink-0">
                      <img src="@/assets/images/user/13.jpg" alt="userimg" class="avatar-48 rounded-circle img-fluid"
                        loading="lazy" />
                    </div>
                    <div class="comment-list-user-data">
                      <div class="d-inline-flex align-items-center gap-1 flex-wrap">
                        <h6 class="m-0">Bob Frapples</h6>
                        <span class="d-inline-block text-primary">
                          <svg class="align-text-bottom" xmlns="http://www.w3.org/2000/svg" width="17" height="17"
                            viewBox="0 0 17 17" fill="none">
                            <path fill-rule="evenodd" clip-rule="evenodd"
                              d="M12.2483 0.216553H4.75081C2.13805 0.216553 0.5 2.0665 0.5 4.68444V11.7487C0.5 14.3666 2.13027 16.2166 4.75081 16.2166H12.2475C14.8689 16.2166 16.5 14.3666 16.5 11.7487V4.68444C16.5 2.0665 14.8689 0.216553 12.2483 0.216553Z"
                              fill="currentColor" />
                            <path d="M5.5 8.21627L7.50056 10.216L11.5 6.21655" stroke="white" stroke-width="1.5"
                              stroke-linecap="round" stroke-linejoin="round" />
                          </svg>
                        </span>
                        <spna class="fw-medium small text-capitalize">3 min ago</spna>
                      </div>
                    </div>
                  </div>
                  <div class="comment-list-user-comment">
                    <div class="comment-list-comment">
                      "Just stumbled upon this post and it's giving me all the
                      feels! 🙌"
                    </div>
                    <div class="comment-list-action mt-2">
                      <ul class="list-inline m-0 p-0 d-flex align-items-center gap-2">
                        <li>
                          <div class="like-block position-relative d-flex align-items-center flex-shrink-0">
                            <div class="like-data">
                              <div class="dropdown">
                                <span class="dropdown-toggle" data-bs-toggle="dropdown" aria-haspopup="true"
                                  aria-expanded="false" role="button">
                                  <span class="material-symbols-outlined align-text-top font-size-18">
                                    thumb_up
                                  </span>
                                  {{''}}
                                  <span class="fw-medium small">Likes</span>
                                </span>
                                <div class="dropdown-menu py-2 shadow">
                                  <a class="ms-2 me-2" href="#" data-bs-toggle="tooltip" data-bs-placement="top"
                                    title="Like"><img src="@/assets/images/icon/01.png" class="img-fluid" alt="like"
                                      loading="lazy" /></a>
                                  <a class="me-2" href="#" data-bs-toggle="tooltip" data-bs-placement="top"
                                    title="Love"><img src="@/assets/images/icon/02.png" class="img-fluid" alt="love"
                                      loading="lazy" /></a>
                                  <a class="me-2" href="#" data-bs-toggle="tooltip" data-bs-placement="top"
                                    title="Happy"><img src="@/assets/images/icon/03.png" class="img-fluid" alt="happy"
                                      loading="lazy" /></a>
                                  <a class="me-2" href="#" data-bs-toggle="tooltip" data-bs-placement="top"
                                    title="HaHa"><img src="@/assets/images/icon/04.png" class="img-fluid" alt="haha"
                                      loading="lazy" /></a>
                                  <a class="me-2" href="#" data-bs-toggle="tooltip" data-bs-placement="top"
                                    title="Think"><img src="@/assets/images/icon/05.png" class="img-fluid" alt="think"
                                      loading="lazy" /></a>
                                  <a class="me-2" href="#" data-bs-toggle="tooltip" data-bs-placement="top"
                                    title="Sad"><img src="@/assets/images/icon/06.png" class="img-fluid" alt="sad"
                                      loading="lazy" /></a>
                                  <a class="me-2" href="#" data-bs-toggle="tooltip" data-bs-placement="top"
                                    title="Lovely"><img src="@/assets/images/icon/07.png" class="img-fluid" alt="lovely"
                                      loading="lazy" /></a>
                                </div>
                              </div>
                            </div>
                          </div>
                        </li>
                        <li>
                          <span class="fw-medium small" data-bs-toggle="collapse" data-bs-target="#subcomment-collapse1"
                            role="button" aria-expanded="false" aria-controls="collapseExample">
                            Reply
                          </span>
                        </li>
                      </ul>
                      <div class="add-comment-form-block collapse mt-3" id="subcomment-collapse1">
                        <div class="d-flex align-items-center gap-3">
                          <div class="flex-shrink-0">
                            <img src="@/assets/images/user/1.jpg" alt="userimg"
                              class="avatar-48 rounded-circle img-fluid" loading="lazy" />
                          </div>
                          <div class="add-comment-form">
                            <form>
                              <input type="text" class="form-control" placeholder="Write a Comment..." />
                              <button type="submit" class="btn btn-primary font-size-12 text-capitalize px-5">
                                post
                              </button>
                            </form>
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </li>
            </ul>
            <div class="add-comment-form-block">
              <div class="d-flex align-items-center gap-3">
                <div class="flex-shrink-0">
                  <img src="@/assets/images/user/1.jpg" alt="userimg" class="avatar-48 rounded-circle img-fluid"
                    loading="lazy" />
                </div>
                <div class="add-comment-form">
                  <form>
                    <input type="text" class="form-control" placeholder="Write a Comment..." />
                    <button type="submit" class="btn btn-primary font-size-12 text-capitalize px-5">
                      post
                    </button>
                  </form>
                </div>
              </div>
            </div>
          </div>
        </div>
        <!-- <div class="comment-area mt-3">
               <div class="d-flex justify-content-between align-items-center flex-wrap">
                  <div class="like-block position-relative d-flex align-items-center">
                     <div class="d-flex align-items-center">
                        <div class="like-data">
                           <div class="dropdown">
                              <span class="dropdown-toggle" data-bs-toggle="dropdown" aria-haspopup="true" aria-expanded="false" role="button">
                              <img src="@/assets/images/icon/01.png" class="img-fluid" alt="">
                              </span>
                              <div class="dropdown-menu py-2">
                                 <a class="ms-2 me-2" href="#" data-bs-toggle="tooltip" data-bs-placement="top" title="Like"><img src="@/assets/images/icon/01.png" class="img-fluid" alt=""></a>
                                 <a class="me-2" href="#"  data-bs-toggle="tooltip" data-bs-placement="top" title="Love"><img src="@/assets/images/icon/02.png" class="img-fluid" alt=""></a>
                                 <a class="me-2" href="#"  data-bs-toggle="tooltip" data-bs-placement="top" title="Happy"><img src="@/assets/images/icon/03.png" class="img-fluid" alt=""></a>
                                 <a class="me-2" href="#"  data-bs-toggle="tooltip" data-bs-placement="top" title="HaHa"><img src="@/assets/images/icon/04.png" class="img-fluid" alt=""></a>
                                 <a class="me-2" href="#"  data-bs-toggle="tooltip" data-bs-placement="top" title="Think"><img src="@/assets/images/icon/05.png" class="img-fluid" alt=""></a>
                                 <a class="me-2" href="#"  data-bs-toggle="tooltip" data-bs-placement="top" title="Sade" ><img src="@/assets/images/icon/06.png" class="img-fluid" alt=""></a>
                                 <a class="me-2" href="#"  data-bs-toggle="tooltip" data-bs-placement="top" title="Lovely"><img src="@/assets/images/icon/07.png" class="img-fluid" alt=""></a>
                              </div>
                           </div>
                        </div>
                        <div class="total-like-block ms-2 me-3">
                           <div class="dropdown">
                              <span class="dropdown-toggle" data-bs-toggle="dropdown" aria-haspopup="true" aria-expanded="false" role="button">
                             me-1  140 Likes
                              </span>
                              <div class="dropdown-menu">
                                 <a class="dropdown-item" href="#">Max Emum</a>
                                 <a class="dropdown-item" href="#">Bill Yerds</a>
                                 <a class="dropdown-item" href="#">Hap E. Birthday</a>
                                 <a class="dropdown-item" href="#">Tara Misu</a>
                                 <a class="dropdown-item" href="#">Midge Itz</a>
                                 <a class="dropdown-item" href="#">Sal Vidge</a>
                                 <a class="dropdown-item" href="#">Other</a>
                              </div>
                           </div>
                        </div>
                     </div>
                     <div class="total-comment-block">
                        <div class="dropdown">
                           <span class="dropdown-toggle" data-bs-toggle="dropdown" aria-haspopup="true" aria-expanded="false" role="button">
                           20 Comment
                           </span>
                           <div class="dropdown-menu">
                              <a class="dropdown-item" href="#">Max Emum</a>
                              <a class="dropdown-item" href="#">Bill Yerds</a>
                              <a class="dropdown-item" href="#">Hap E. Birthday</a>
                              <a class="dropdown-item" href="#">Tara Misu</a>
                              <a class="dropdown-item" href="#">Midge Itz</a>
                              <a class="dropdown-item" href="#">Sal Vidge</a>
                              <a class="dropdown-item" href="#">Other</a>
                           </div>
                        </div>
                     </div>
                  </div>
                 <div class="share-block d-flex align-items-center feather-icon mt-2 mt-md-0">
                           <a href="#" data-bs-toggle="offcanvas" data-bs-target="#share-btn" aria-controls="share-btn" class="d-flex align-items-center"><span class="material-symbols-outlined md-18">
                           share
                           </span>
                           <span class="ms-1">99 Share</span></a>
                        </div>
                  <offcanvas mainClass="bottom share-offcanvas" tabindex="-1" id="shareBottom1" ariaLabelled="shareBottom1Label">
                     <offcanvas-header>
                        <h5 class="offcanvas-title" id="shareBottom1Label">Share</h5>
                        <button type="button" class="btn-close text-reset" data-bs-dismiss="offcanvas" aria-label="Close"></button>
                     </offcanvas-header>
                     <offcanvas-body bodyClass="small">
                        <div class="d-flex flex-wrap align-items-center">
                           <div class="text-center me-3 mb-3">
                              <img src="@/assets/images/icon/08.png" class="img-fluid mb-2" alt="">
                              <h6>Facebook</h6>
                           </div>
                           <div class="text-center me-3 mb-3">
                              <img src="@/assets/images/icon/09.png" class="img-fluid mb-2" alt="">
                              <h6>Twitter</h6>
                           </div>
                           <div class="text-center me-3 mb-3">
                              <img src="@/assets/images/icon/10.png" class="img-fluid mb-2" alt="">
                              <h6>Instagram</h6>
                           </div>
                           <div class="text-center me-3 mb-3">
                              <img src="@/assets/images/icon/11.png" class="img-fluid mb-2" alt="">
                              <h6>Google Plus</h6>
                           </div>
                           <div class="text-center me-3 mb-3">
                              <img src="@/assets/images/icon/13.png" class="img-fluid mb-2" alt="">
                              <h6>In</h6>
                           </div>
                           <div class="text-center me-3 mb-3">
                              <img src="@/assets/images/icon/12.png" class="img-fluid mb-2" alt="">
                              <h6>YouTube</h6>
                           </div>
                        </div>
                     </offcanvas-body>
                  </offcanvas>
               </div>
               <hr>
               <ul class="post-comments list-inline p-0 m-0">
                  <li class="mb-2">
                     <div class="d-flex ">
                        <div class="user-img">
                           <img src="@/assets/images/user/02.jpg" alt="userimg" class="avatar-35 rounded-circle img-fluid">
                        </div>
                        <div class="comment-data-block ms-3">
                           <h6>Monty Carlo</h6>
                           <p class="mb-0">Lorem ipsum dolor sit amet</p>
                           <div class="d-flex flex-wrap align-items-center comment-activity">
                              <a href="#">like</a>
                              <a href="#">reply</a>
                              <a href="#">translate</a>
                              <span> 5 min </span>
                           </div>
                        </div>
                     </div>
                  </li>
                  <li>
                     <div class="d-flex ">
                        <div class="user-img">
                           <img src="@/assets/images/user/03.jpg" alt="userimg" class="avatar-35 rounded-circle img-fluid">
                        </div>
                        <div class="comment-data-block ms-3">
                           <h6>Paul Molive</h6>
                           <p class="mb-0">Lorem ipsum dolor sit amet</p>
                           <div class="d-flex flex-wrap align-items-center comment-activity">
                              <a href="#">like</a>
                              <a href="#">reply</a>
                              <a href="#">translate</a>
                              <span> 5 min </span>
                           </div>
                        </div>
                     </div>
                  </li>
               </ul>
               <form class="comment-text d-flex align-items-center mt-3" action="#">
                  <input type="text" class="form-control rounded" placeholder="Enter Your Comment">
                 <div class="comment-attagement d-flex align-items-center">
                           <a href="#" class="material-symbols-outlined me-3 link">
                           insert_link
                           </a>
                           <a href="#" class="material-symbols-outlined  me-3">
                           sentiment_satisfied
                           </a>
                           <a href="#" class="material-symbols-outlined  me-3">
                           photo_camera
                           </a>
                        </div>
               </form>
            </div> -->
      </b-card-body>
    </b-card>
  </b-col>
  <b-col sm="12" class="social-post">
    <b-card no-body class="card-block card-stretch card-height">
      <b-card-body>
        <div class="user-post-data">
          <div class="d-flex align-items-center justify-content-between">
            <div class="me-3 flex-shrik-0">
              <img class="border border-2 rounded-circle user-post-profile" src="@/assets/images/user/04.jpg"
                alt="user-image" loading="lazy" />
            </div>
            <div class="w-100">
              <div class="d-flex align-items-center justify-content-between">
                <div>
                  <h6 class="mb-0 d-inline-block">Ira Membrit</h6>{{ "" }}
                  <span class="d-inline-block text-primary">
                    <svg class="align-text-bottom" width="17" height="17" viewBox="0 0 17 17" fill="none"
                      xmlns="http://www.w3.org/2000/svg">
                      <path fill-rule="evenodd" clip-rule="evenodd"
                        d="M11.8457 0H4.34822C1.73547 0 0.0974121 1.84995 0.0974121 4.46789V11.5321C0.0974121 14.1501 1.72768 16 4.34822 16H11.8449C14.4663 16 16.0974 14.1501 16.0974 11.5321V4.46789C16.0974 1.84995 14.4663 0 11.8457 0Z"
                        fill="currentColor" />
                      <path d="M5.09741 7.99978L7.09797 9.9995L11.0974 6.00006" stroke="white" stroke-width="1.5"
                        stroke-linecap="round" stroke-linejoin="round" />
                    </svg>
                  </span>{{ "" }}
                  <span class="mb-0 d-inline-block text-capitalize fw-medium">Update her Status</span>
                  <p class="mb-0">6 Hours ago</p>
                </div>
                <div class="card-post-toolbar">
                  <div class="dropdown">
                    <span class="dropdown-toggle material-symbols-outlined" data-bs-toggle="dropdown"
                      aria-haspopup="true" aria-expanded="false" role="button">
                      more_horiz
                    </span>
                    <div class="dropdown-menu m-0 p-0">
                      <a class="dropdown-item p-3" href="#">
                        <div class="d-flex align-items-top">
                          <span class="material-symbols-outlined"> save </span>
                          <div class="data ms-2">
                            <h6>Save Post</h6>
                            <p class="mb-0">Add this to your saved items</p>
                          </div>
                        </div>
                      </a>
                      <a class="dropdown-item p-3" href="#">
                        <div class="d-flex align-items-top">
                          <span class="material-symbols-outlined">
                            cancel
                          </span>
                          <div class="data ms-2">
                            <h6>Hide Post</h6>
                            <p class="mb-0">See fewer posts like this.</p>
                          </div>
                        </div>
                      </a>
                      <a class="dropdown-item p-3" href="#">
                        <div class="d-flex align-items-top">
                          <span class="material-symbols-outlined">
                            person_remove
                          </span>
                          <div class="data ms-2">
                            <h6>Unfollow User</h6>
                            <p class="mb-0">
                              Stop seeing posts but stay friends.
                            </p>
                          </div>
                        </div>
                      </a>

                      <a class="dropdown-item p-3" href="#">
                        <div class="d-flex align-items-top">
                          <span class="material-symbols-outlined">
                            notifications
                          </span>
                          <div class="data ms-2">
                            <h6>Notifications</h6>
                            <p class="mb-0">
                              Turn on notifications for this post
                            </p>
                          </div>
                        </div>
                      </a>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="mt-4">
          <p class="m-0">
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi
            nulla dolor, ornare at commodo non, feugiat non nisi. Phasellus
            faucibus mollis pharetra. Proin blandit ac massa sed rhoncus"
          </p>
        </div>
        <div class="post-meta-likes mt-4">
          <div class="d-flex align-items-center gap-2 flex-wrap">
            <ul class="list-inline m-0 p-0 post-user-liked-list">
              <li>
                <img src="@/assets/images/user/01.jpg" alt="userimg" class="rounded-circle img-fluid userimg"
                  loading="lazy" />
              </li>
              {{
                ""
              }}
              <li>
                <img src="@/assets/images/user/02.jpg" alt="userimg" class="rounded-circle img-fluid userimg"
                  loading="lazy" />
              </li>
              {{
                ""
              }}
              <li>
                <img src="@/assets/images/user/03.jpg" alt="userimg" class="rounded-circle img-fluid userimg"
                  loading="lazy" />
              </li>
              {{
                ""
              }}
              <li>
                <img src="@/assets/images/user/04.jpg" alt="userimg" class="rounded-circle img-fluid userimg"
                  loading="lazy" />
              </li>
            </ul>
            <div class="d-inline-flex align-items-center gap-1">
              <h6 class="m-0 font-size-14">Aliana Molex</h6>
              <span class="text-capitalize font-size-14 fw-medium" type="button" data-bs-toggle="modal"
                data-bs-target="#likemodal">and 208 others liked this</span>
            </div>
          </div>
        </div>
        <div class="comment-area mt-4 pt-4 border-top">
          <div class="d-flex justify-content-between align-items-center flex-wrap">
            <div class="like-block position-relative d-flex align-items-center flex-shrink-0">
              <div class="like-data">
                <div class="dropdown">
                  <span class="dropdown-toggle" data-bs-toggle="dropdown" aria-haspopup="true" aria-expanded="false"
                    role="button">
                    <span class="material-symbols-outlined align-text-top font-size-20">
                      thumb_up
                    </span>{{ "" }}
                    <span class="fw-medium">140 Likes</span>
                  </span>
                  <div class="dropdown-menu py-2 shadow">
                    <a class="ms-2 me-2" href="#" v-b-tooltip.hover title="Like"><img src="@/assets/images/icon/01.png"
                        class="img-fluid" alt="like" loading="lazy" /></a>

                    <a class="me-2" href="#" v-b-tooltip.hover title="Love"><img src="@/assets/images/icon/02.png"
                        class="img-fluid" alt="love" loading="lazy" /></a>
                    <a class="me-2" href="#" v-b-tooltip.hover title="Happy"><img src="@/assets/images/icon/03.png"
                        class="img-fluid" alt="happy" loading="lazy" /></a>
                    <a class="me-2" href="#" v-b-tooltip.hover title="HaHa"><img src="@/assets/images/icon/04.png"
                        class="img-fluid" alt="haha" loading="lazy" /></a>
                    <a class="me-2" href="#" v-b-tooltip.hover title="Think"><img src="@/assets/images/icon/05.png"
                        class="img-fluid" alt="think" loading="lazy" /></a>
                    <a class="me-2" href="#" v-b-tooltip.hover title="Sad"><img src="@/assets/images/icon/06.png"
                        class="img-fluid" alt="sad" loading="lazy" /></a>
                    <a class="me-2" href="#" v-b-tooltip.hover title="Lovely"><img src="@/assets/images/icon/07.png"
                        class="img-fluid" alt="lovely" loading="lazy" /></a>
                  </div>
                </div>
              </div>
            </div>
            <div class="d-flex align-items-center gap-3 flex-shrink-0">
              <div class="total-comment-block" type="button" data-bs-toggle="collapse"
                data-bs-target="#commentcollapes3" aria-expanded="false" aria-controls="commentcollapes">
                <span class="material-symbols-outlined align-text-top font-size-20">
                  comment
                </span>
                {{ "" }}
                <span class="fw-medium">20 Comment</span>
              </div>
              <div class="share-block d-flex align-items-center feather-icon">
                <a href="#" data-bs-toggle="modal" data-bs-target="#modal-share-offcanvas" aria-controls="share-btn"
                  class="d-flex align-items-center">
                  <span class="material-symbols-outlined align-text-top font-size-20">
                    share
                  </span>
                  <span class="ms-1 fw-medium">99 Share</span></a>
                <ShareOffcanvas />
              </div>
            </div>
          </div>
          <div class="collapse mt-4 pt-4 border-top" id="commentcollapes3">
            <ul class="list-inline m-o p-0 comment-list">
              <li class="mb-3">
                <div class="comment-list-block">
                  <div class="d-flex align-items-center gap-3">
                    <div class="comment-list-user-img flex-shrink-0">
                      <img src="@/assets/images/user/13.jpg" alt="userimg" class="avatar-48 rounded-circle img-fluid"
                        loading="lazy" />
                    </div>
                    <div class="comment-list-user-data">
                      <div class="d-inline-flex align-items-center gap-1 flex-wrap">
                        <h6 class="m-0">Bob Frapples</h6>
                        <span class="d-inline-block text-primary">
                          <svg class="align-text-bottom" xmlns="http://www.w3.org/2000/svg" width="17" height="17"
                            viewBox="0 0 17 17" fill="none">
                            <path fill-rule="evenodd" clip-rule="evenodd"
                              d="M12.2483 0.216553H4.75081C2.13805 0.216553 0.5 2.0665 0.5 4.68444V11.7487C0.5 14.3666 2.13027 16.2166 4.75081 16.2166H12.2475C14.8689 16.2166 16.5 14.3666 16.5 11.7487V4.68444C16.5 2.0665 14.8689 0.216553 12.2483 0.216553Z"
                              fill="currentColor" />
                            <path d="M5.5 8.21627L7.50056 10.216L11.5 6.21655" stroke="white" stroke-width="1.5"
                              stroke-linecap="round" stroke-linejoin="round" />
                          </svg>
                        </span>
                        <spna class="fw-medium small text-capitalize">3 min ago</spna>
                      </div>
                    </div>
                  </div>
                  <div class="comment-list-user-comment">
                    <div class="comment-list-comment">
                      "Just stumbled upon this post and it's giving me all the
                      feels! 🙌"
                    </div>
                    <div class="comment-list-action mt-2">
                      <ul class="list-inline m-0 p-0 d-flex align-items-center gap-2">
                        <li>
                          <div class="like-block position-relative d-flex align-items-center flex-shrink-0">
                            <div class="like-data">
                              <div class="dropdown">
                                <span class="dropdown-toggle" data-bs-toggle="dropdown" aria-haspopup="true"
                                  aria-expanded="false" role="button">
                                  <span class="material-symbols-outlined align-text-top font-size-18">
                                    thumb_up
                                  </span>
                                  {{''}}
                                  <span class="fw-medium small">Likes</span>
                                </span>
                                <div class="dropdown-menu py-2 shadow">
                                  <a class="ms-2 me-2" href="#" data-bs-toggle="tooltip" data-bs-placement="top"
                                    title="Like"><img src="@/assets/images/icon/01.png" class="img-fluid" alt="like"
                                      loading="lazy" /></a>
                                  <a class="me-2" href="#" data-bs-toggle="tooltip" data-bs-placement="top"
                                    title="Love"><img src="@/assets/images/icon/02.png" class="img-fluid" alt="love"
                                      loading="lazy" /></a>
                                  <a class="me-2" href="#" data-bs-toggle="tooltip" data-bs-placement="top"
                                    title="Happy"><img src="@/assets/images/icon/03.png" class="img-fluid" alt="happy"
                                      loading="lazy" /></a>
                                  <a class="me-2" href="#" data-bs-toggle="tooltip" data-bs-placement="top"
                                    title="HaHa"><img src="@/assets/images/icon/04.png" class="img-fluid" alt="haha"
                                      loading="lazy" /></a>
                                  <a class="me-2" href="#" data-bs-toggle="tooltip" data-bs-placement="top"
                                    title="Think"><img src="@/assets/images/icon/05.png" class="img-fluid" alt="think"
                                      loading="lazy" /></a>
                                  <a class="me-2" href="#" data-bs-toggle="tooltip" data-bs-placement="top"
                                    title="Sad"><img src="@/assets/images/icon/06.png" class="img-fluid" alt="sad"
                                      loading="lazy" /></a>
                                  <a class="me-2" href="#" data-bs-toggle="tooltip" data-bs-placement="top"
                                    title="Lovely"><img src="@/assets/images/icon/07.png" class="img-fluid" alt="lovely"
                                      loading="lazy" /></a>
                                </div>
                              </div>
                            </div>
                          </div>
                        </li>
                        <li>
                          <span class="fw-medium small" data-bs-toggle="collapse" data-bs-target="#subcomment-collapse3"
                            role="button" aria-expanded="false" aria-controls="collapseExample">
                            Reply
                          </span>
                        </li>
                      </ul>
                      <div class="add-comment-form-block collapse mt-3" id="subcomment-collapse3">
                        <div class="d-flex align-items-center gap-3">
                          <div class="flex-shrink-0">
                            <img src="@/assets/images/user/1.jpg" alt="userimg"
                              class="avatar-48 rounded-circle img-fluid" loading="lazy" />
                          </div>
                          <div class="add-comment-form">
                            <form>
                              <input type="text" class="form-control" placeholder="Write a Comment..." />
                              <button type="submit" class="btn btn-primary font-size-12 text-capitalize px-5">
                                post
                              </button>
                            </form>
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </li>
            </ul>
            <div class="add-comment-form-block">
              <div class="d-flex align-items-center gap-3">
                <div class="flex-shrink-0">
                  <img src="@/assets/images/user/1.jpg" alt="userimg" class="avatar-48 rounded-circle img-fluid"
                    loading="lazy" />
                </div>
                <div class="add-comment-form">
                  <form>
                    <input type="text" class="form-control" placeholder="Write a Comment..." />
                    <button type="submit" class="btn btn-primary font-size-12 text-capitalize px-5">
                      post
                    </button>
                  </form>
                </div>
              </div>
            </div>
          </div>
        </div>
      </b-card-body>
    </b-card>
  </b-col>
  <div sm="12" class="social-post">
    <b-card no-body class="card-block card-stretch card-height">
      <b-card-body>
        <div class="user-post-data">
          <div class="d-flex align-items-center justify-content-between">
            <div class="me-3 flex-shrik-0">
              <img class="border border-2 rounded-circle user-post-profile" src="@/assets/images/user/1.jpg"
                alt="user-image" loading="lazy" />
            </div>
            <div class="w-100">
              <div class="d-flex align-items-center justify-content-between">
                <div>
                  <h6 class="mb-0 d-inline-block">Bni Cyst</h6>{{ "" }}
                  <span class="d-inline-block text-primary">
                    <svg class="align-text-bottom" width="17" height="17" viewBox="0 0 17 17" fill="none"
                      xmlns="http://www.w3.org/2000/svg">
                      <path fill-rule="evenodd" clip-rule="evenodd"
                        d="M11.8457 0H4.34822C1.73547 0 0.0974121 1.84995 0.0974121 4.46789V11.5321C0.0974121 14.1501 1.72768 16 4.34822 16H11.8449C14.4663 16 16.0974 14.1501 16.0974 11.5321V4.46789C16.0974 1.84995 14.4663 0 11.8457 0Z"
                        fill="currentColor" />
                      <path d="M5.09741 7.99978L7.09797 9.9995L11.0974 6.00006" stroke="white" stroke-width="1.5"
                        stroke-linecap="round" stroke-linejoin="round" />
                    </svg>
                  </span>{{ "" }}
                  <span class="mb-0 d-inline-block text-capitalize fw-medium">Added New Video in his Timeline</span>
                  <p class="mb-0">8 Hours ago</p>
                </div>
                <div class="card-post-toolbar">
                  <div class="dropdown">
                    <span class="dropdown-toggle material-symbols-outlined" data-bs-toggle="dropdown"
                      aria-haspopup="true" aria-expanded="false" role="button">
                      more_horiz
                    </span>
                    <div class="dropdown-menu m-0 p-0">
                      <a class="dropdown-item p-3" href="#">
                        <div class="d-flex align-items-top">
                          <span class="material-symbols-outlined"> save </span>
                          <div class="data ms-2">
                            <h6>Save Post</h6>
                            <p class="mb-0">Add this to your saved items</p>
                          </div>
                        </div>
                      </a>
                      <a class="dropdown-item p-3" href="#">
                        <div class="d-flex align-items-top">
                          <span class="material-symbols-outlined">
                            cancel
                          </span>
                          <div class="data ms-2">
                            <h6>Hide Post</h6>
                            <p class="mb-0">See fewer posts like this.</p>
                          </div>
                        </div>
                      </a>
                      <a class="dropdown-item p-3" href="#">
                        <div class="d-flex align-items-top">
                          <span class="material-symbols-outlined">
                            person_remove
                          </span>
                          <div class="data ms-2">
                            <h6>Unfollow User</h6>
                            <p class="mb-0">
                              Stop seeing posts but stay friends.
                            </p>
                          </div>
                        </div>
                      </a>

                      <a class="dropdown-item p-3" href="#">
                        <div class="d-flex align-items-top">
                          <span class="material-symbols-outlined">
                            notifications
                          </span>
                          <div class="data ms-2">
                            <h6>Notifications</h6>
                            <p class="mb-0">
                              Turn on notifications for this post
                            </p>
                          </div>
                        </div>
                      </a>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="mt-4">
          <p class="m-0">
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi
            nulla dolor, ornare at commodo non, feugiat non nisi. Phasellus
            faucibus mollis pharetra. Proin blandit ac massa sed rhoncus"
          </p>
        </div>
        <div class="user-post mt-4">
          <div class="ratio ratio-16x9">
            <iframe src="https://www.youtube.com/embed/oHD33oKbKh4?si=VF-Qcp-pZdzUb3RX" allowfullscreen></iframe>
          </div>
        </div>
        <div class="post-meta-likes mt-4">
          <div class="d-flex align-items-center gap-2 flex-wrap">
            <ul class="list-inline m-0 p-0 post-user-liked-list">
              <li>
                <img src="@/assets/images/user/01.jpg" alt="userimg" class="rounded-circle img-fluid userimg"
                  loading="lazy" />
              </li>
              {{
                ""
              }}
              <li>
                <img src="@/assets/images/user/02.jpg" alt="userimg" class="rounded-circle img-fluid userimg"
                  loading="lazy" />
              </li>
              {{
                ""
              }}
              <li>
                <img src="@/assets/images/user/03.jpg" alt="userimg" class="rounded-circle img-fluid userimg"
                  loading="lazy" />
              </li>
              {{
                ""
              }}
              <li>
                <img src="@/assets/images/user/04.jpg" alt="userimg" class="rounded-circle img-fluid userimg"
                  loading="lazy" />
              </li>
            </ul>
            <div class="d-inline-flex align-items-center gap-1">
              <h6 class="m-0 font-size-14">Aliana Molex</h6>
              <span class="text-capitalize font-size-14 fw-medium" type="button" data-bs-toggle="modal"
                data-bs-target="#likemodal">and 208 others liked this</span>
            </div>
          </div>
        </div>
        <div class="comment-area mt-4 pt-4 border-top">
          <div class="d-flex justify-content-between align-items-center flex-wrap">
            <div class="like-block position-relative d-flex align-items-center flex-shrink-0">
              <div class="like-data">
                <div class="dropdown">
                  <span class="dropdown-toggle" data-bs-toggle="dropdown" aria-haspopup="true" aria-expanded="false"
                    role="button">
                    <span class="material-symbols-outlined align-text-top font-size-20">
                      thumb_up
                    </span>{{ "" }}
                    <span class="fw-medium">140 Likes</span>
                  </span>
                  <div class="dropdown-menu py-2 shadow">
                    <a class="ms-2 me-2" href="#" v-b-tooltip.hover title="Like"><img src="@/assets/images/icon/01.png"
                        class="img-fluid" alt="like" loading="lazy" /></a>
                    <a class="me-2" href="#" v-b-tooltip.hover title="Love"><img src="@/assets/images/icon/02.png"
                        class="img-fluid" alt="love" loading="lazy" /></a>
                    <a class="me-2" href="#" v-b-tooltip.hover title="Happy"><img src="@/assets/images/icon/03.png"
                        class="img-fluid" alt="happy" loading="lazy" /></a>
                    <a class="me-2" href="#" v-b-tooltip.hover title="HaHa"><img src="@/assets/images/icon/04.png"
                        class="img-fluid" alt="haha" loading="lazy" /></a>
                    <a class="me-2" href="#" v-b-tooltip.hover title="Think"><img src="@/assets/images/icon/05.png"
                        class="img-fluid" alt="think" loading="lazy" /></a>
                    <a class="me-2" href="#" v-b-tooltip.hover title="Sad"><img src="@/assets/images/icon/06.png"
                        class="img-fluid" alt="sad" loading="lazy" /></a>
                    <a class="me-2" href="#" v-b-tooltip.hover title="Lovely"><img src="@/assets/images/icon/07.png"
                        class="img-fluid" alt="lovely" loading="lazy" /></a>
                  </div>
                </div>
              </div>
            </div>
            <div class="d-flex align-items-center gap-3 flex-shrink-0">
              <div class="total-comment-block" type="button" data-bs-toggle="collapse"
                data-bs-target="#commentcollapes4" aria-expanded="false" aria-controls="commentcollapes">
                <span class="material-symbols-outlined align-text-top font-size-20">
                  comment
                </span>
                {{ "" }}
                <span class="fw-medium">20 Comment</span>
              </div>
              <div class="share-block d-flex align-items-center feather-icon">
                <a href="#" data-bs-toggle="modal" data-bs-target="#modal-share-offcanvas" aria-controls="share-btn"
                  class="d-flex align-items-center">
                  <span class="material-symbols-outlined align-text-top font-size-20">
                    share
                  </span>
                  <span class="ms-1 fw-medium">99 Share</span></a>
                <ShareOffcanvas />
              </div>
            </div>
          </div>
          <div class="collapse mt-4 pt-4 border-top" id="commentcollapes4">
            <ul class="list-inline m-o p-0 comment-list">
              <li class="mb-3">
                <div class="comment-list-block">
                  <div class="d-flex align-items-center gap-3">
                    <div class="comment-list-user-img flex-shrink-0">
                      <img src="@/assets/images/user/13.jpg" alt="userimg" class="avatar-48 rounded-circle img-fluid"
                        loading="lazy" />
                    </div>
                    <div class="comment-list-user-data">
                      <div class="d-inline-flex align-items-center gap-1 flex-wrap">
                        <h6 class="m-0">Bob Frapples</h6>
                        <span class="d-inline-block text-primary">
                          <svg class="align-text-bottom" xmlns="http://www.w3.org/2000/svg" width="17" height="17"
                            viewBox="0 0 17 17" fill="none">
                            <path fill-rule="evenodd" clip-rule="evenodd"
                              d="M12.2483 0.216553H4.75081C2.13805 0.216553 0.5 2.0665 0.5 4.68444V11.7487C0.5 14.3666 2.13027 16.2166 4.75081 16.2166H12.2475C14.8689 16.2166 16.5 14.3666 16.5 11.7487V4.68444C16.5 2.0665 14.8689 0.216553 12.2483 0.216553Z"
                              fill="currentColor" />
                            <path d="M5.5 8.21627L7.50056 10.216L11.5 6.21655" stroke="white" stroke-width="1.5"
                              stroke-linecap="round" stroke-linejoin="round" />
                          </svg>
                        </span>
                        <spna class="fw-medium small text-capitalize">3 min ago</spna>
                      </div>
                    </div>
                  </div>
                  <div class="comment-list-user-comment">
                    <div class="comment-list-comment">
                      "Just stumbled upon this post and it's giving me all the
                      feels! 🙌"
                    </div>
                    <div class="comment-list-action mt-2">
                      <ul class="list-inline m-0 p-0 d-flex align-items-center gap-2">
                        <li>
                          <div class="like-block position-relative d-flex align-items-center flex-shrink-0">
                            <div class="like-data">
                              <div class="dropdown">
                                <span class="dropdown-toggle" data-bs-toggle="dropdown" aria-haspopup="true"
                                  aria-expanded="false" role="button">
                                  <span class="material-symbols-outlined align-text-top font-size-18">
                                    thumb_up
                                  </span>
                                  {{''}}
                                  <span class="fw-medium small">Likes</span>
                                </span>
                                <div class="dropdown-menu py-2 shadow">
                                  <a class="ms-2 me-2" href="#" data-bs-toggle="tooltip" data-bs-placement="top"
                                    title="Like"><img src="@/assets/images/icon/01.png" class="img-fluid" alt="like"
                                      loading="lazy" /></a>
                                  <a class="me-2" href="#" data-bs-toggle="tooltip" data-bs-placement="top"
                                    title="Love"><img src="@/assets/images/icon/02.png" class="img-fluid" alt="love"
                                      loading="lazy" /></a>
                                  <a class="me-2" href="#" data-bs-toggle="tooltip" data-bs-placement="top"
                                    title="Happy"><img src="@/assets/images/icon/03.png" class="img-fluid" alt="happy"
                                      loading="lazy" /></a>
                                  <a class="me-2" href="#" data-bs-toggle="tooltip" data-bs-placement="top"
                                    title="HaHa"><img src="@/assets/images/icon/04.png" class="img-fluid" alt="haha"
                                      loading="lazy" /></a>
                                  <a class="me-2" href="#" data-bs-toggle="tooltip" data-bs-placement="top"
                                    title="Think"><img src="@/assets/images/icon/05.png" class="img-fluid" alt="think"
                                      loading="lazy" /></a>
                                  <a class="me-2" href="#" data-bs-toggle="tooltip" data-bs-placement="top"
                                    title="Sad"><img src="@/assets/images/icon/06.png" class="img-fluid" alt="sad"
                                      loading="lazy" /></a>
                                  <a class="me-2" href="#" data-bs-toggle="tooltip" data-bs-placement="top"
                                    title="Lovely"><img src="@/assets/images/icon/07.png" class="img-fluid" alt="lovely"
                                      loading="lazy" /></a>
                                </div>
                              </div>
                            </div>
                          </div>
                        </li>
                        <li>
                          <span class="fw-medium small" data-bs-toggle="collapse" data-bs-target="#subcomment-collapse4"
                            role="button" aria-expanded="false" aria-controls="collapseExample">
                            Reply
                          </span>
                        </li>
                      </ul>
                      <div class="add-comment-form-block collapse mt-3" id="subcomment-collapse4">
                        <div class="d-flex align-items-center gap-3">
                          <div class="flex-shrink-0">
                            <img src="@/assets/images/user/1.jpg" alt="userimg"
                              class="avatar-48 rounded-circle img-fluid" loading="lazy" />
                          </div>
                          <div class="add-comment-form">
                            <form>
                              <input type="text" class="form-control" placeholder="Write a Comment..." />
                              <button type="submit" class="btn btn-primary font-size-12 text-capitalize px-5">
                                post
                              </button>
                            </form>
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </li>
            </ul>
            <div class="add-comment-form-block">
              <div class="d-flex align-items-center gap-3">
                <div class="flex-shrink-0">
                  <img src="@/assets/images/user/1.jpg" alt="userimg" class="avatar-48 rounded-circle img-fluid"
                    loading="lazy" />
                </div>
                <div class="add-comment-form">
                  <form>
                    <input type="text" class="form-control" placeholder="Write a Comment..." />
                    <button type="submit" class="btn btn-primary font-size-12 text-capitalize px-5">
                      post
                    </button>
                  </form>
                </div>
              </div>
            </div>
          </div>
        </div>
      </b-card-body>
    </b-card>
  </div>

  <FsLightbox :toggler="toggler" :sources="[
    require('@/assets/images/page-img/fun.jpg'),
    require('@/assets/images/page-img/boy.jpg'),
    require('@/assets/images/page-img/bus.jpg'),
    require('@/assets/images/page-img/fd.jpg'),
    require('@/assets/images/page-img/mountain.jpg'),
    require('@/assets/images/page-img/pizza.jpg'),
  ]" />
</template>
<script>
import FsLightbox from "fslightbox-vue/v3";
import ShareOffcanvas from "@/components/shareOffcanvas.vue";
export default {
  name: "SocialPost",
  props: ["post"],
  components: { FsLightbox, ShareOffcanvas },
  data() {
    return {
      commentMessage: "",
      toggler: false,
      // toggler1:false
    };
  },
  methods: {
    addDataDismiss() {
      var els = document.querySelectorAll('.btn-close');
      for (var i = 0; i < els.length; i++) {
        els[i].setAttribute("data-bs-dismiss", "modal");
      }
    }
  },
  mounted() {
    // Call addDataDismiss when the component is mounted
    this.addDataDismiss();
  }
};
</script>
