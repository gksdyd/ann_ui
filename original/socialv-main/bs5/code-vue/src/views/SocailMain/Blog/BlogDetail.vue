<template>
  <div class="content-inner">
    <b-container>
      <b-row>
        <b-col lg="8">
          <b-card no-body class="card-block card-stretch card-height blog blog-detail">
            <b-card-body>
              <div class="image-block">
                <img src="@/assets/images/blog/01.jpg" class="img-fluid rounded w-100" alt="blog-img" />
              </div>
              <div class="blog-description mt-3">
                <h5 class="mb-3 pb-3 border-bottom">
                  There are many variations of passages.
                </h5>
                <div class="blog-meta d-flex align-items-center mb-3 position-right-side flex-wrap">
                  <div class="date me-4 d-flex align-items-center">
                    <i class="material-symbols-outlined pe-2 md-18 text-primary">calendar_month</i>2 Weeks ago
                  </div>
                  <div class="like me-4 d-flex align-items-center">
                    <i class="material-symbols-outlined pe-2 md-18 text-primary">
                      thumb_up_alt </i>20 Like
                  </div>
                  <div class="comments me-4 d-flex align-items-center">
                    <i class="material-symbols-outlined pe-2 md-18 text-primary">
                      mode_comment </i>82 Comments
                  </div>
                  <div class="share d-flex align-items-center">
                    <i class="material-symbols-outlined pe-2 md-18 text-primary">
                      share </i>Share
                  </div>
                </div>
                <p>
                  Voluptatem accusantium doloremque laudantium, totam rem
                  aperiam, eaque ipsa quae ab illo inventore veritatis et quasi
                  architecto beatae vitae dicta sunt explicabo. Nemo enim ipsam
                  voluptatem quia voluptas sit aspernatur aut odit aut fugit,
                  sed quia consequuntur magni dolores eos qui ratione voluptatem
                  sequi nesciunt.
                </p>
                <a href="#" class="d-flex align-items-center" tabindex="-1">Read More
                  <i class="material-symbols-outlined fs-6">arrow_forward_ios</i></a>
              </div>
            </b-card-body>
          </b-card>
        </b-col>
        <b-col lg="4">
          <b-card no-body class="card-block card-stretch card-height blog-post">
            <div class="card-header d-flex justify-content-between">
              <div class="header-title">
                <h4 class="card-title">New Post</h4>
              </div>
            </div>
            <b-card-body class="pt-0">
              <ul class="list-inline p-0 m-0">
                <li v-for="(item, index) in blogPosts" :key="index" :class="item.mbclass">
                  <b-row :class="`align-items-top ${item.borderBottom}`">
                    <b-col md="5">
                      <div class="image-block">
                        <img :src="item.imageSrc" class="img-fluid rounded w-100" :alt="'blog-img-' + index" />
                      </div>
                    </b-col>
                    <b-col md="7">
                      <div class="blog-description mt-1 mt-md-0">
                        <div class="date mb-1">
                          <a href="#" tabindex="-1">{{ item.date }}</a>
                        </div>
                        <h6>{{ item.title }}</h6>
                      </div>
                    </b-col>
                  </b-row>
                </li>
              </ul>
            </b-card-body>
          </b-card>
        </b-col>
        <b-col lg="12">
          <b-card no-body class="card-block card-stretch card-height blog user-comment">
            <div class="card-header d-flex justify-content-between">
              <div class="header-title">
                <h4 class="card-title">User Comment</h4>
              </div>
            </div>
            <b-card-body class="pt-0">
              <b-row>
                <b-col lg="12">
                  <b-card no-body class="card-block card-stretch card-height blog">
                    <b-card-body class="p-0">
                      <div class="d-flex align-items-center">
                        <div class="user-image mb-3">
                          <img class="avatar-80 rounded" src="@/assets/images/user/01.jpg" alt="#"
                            data-original-title="" title="" loading="lazy" />
                        </div>
                        <div class="ms-3">
                          <h5>Kaya Scodelario</h5>
                          <p>Web Developer</p>
                        </div>
                      </div>
                      <div class="blog-description">
                        <p>
                          At vero eos et accusamus et iusto odio dignissimos
                          ducimus qui blanditiis praesentium voluptatum atque
                          corrupti quos dolores et quas molestias excepturi sint
                          occaecati cupiditate non provident.
                        </p>
                        <div class="d-flex align-items-center justify-content-between mb-2 position-right-side">
                          <a href="#" class="comments d-flex align-items-center"><i
                              class="material-symbols-outlined pe-2 md-18 text-primary">
                              mode_comment </i>82 comments</a>
                          <span class="text-warning d-block line-height">
                            <i class="material-symbols-outlined md-18">star_half</i>
                            {{ "" }}
                            <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                            <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                            <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                            <i class="material-symbols-outlined md-18">star</i>
                          </span>
                        </div>
                      </div>
                    </b-card-body>
                  </b-card>
                </b-col>
                <b-col lg="12" class="ps-0 ps-md-5">
                  <b-card no-body class="card-block card-stretch card-height blog">
                    <b-card-body class="p-0">
                      <div class="d-flex align-items-center">
                        <div class="user-image mb-3">
                          <img class="avatar-80 rounded" src="@/assets/images/user/02.jpg" alt="#"
                            data-original-title="" title="" />
                        </div>
                        <div class="ms-3">
                          <h5>Tom Cruise</h5>
                          <p>Web Designer</p>
                        </div>
                      </div>
                      <div class="blog-description">
                        <p>
                          It is a long established fact that a reader will be
                          distracted by the readable content of a page when
                          looking at its layout. The point of using Lorem Ipsum
                          Many desktop publishing packages and web page editors
                          now use Lorem Ipsum.
                        </p>
                        <div class="d-flex align-items-center justify-content-between mb-2 position-right-side">
                          <a href="#" class="comments d-flex align-items-center"><i
                              class="material-symbols-outlined pe-2 md-18 text-primary">
                              mode_comment </i>98 comments</a>
                          <span class="font-size-12 text-warning">
                            <i class="material-symbols-outlined md-18">star_half</i>{{ "" }}
                            <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                            <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                            <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                            <i class="material-symbols-outlined md-18">star</i>
                          </span>
                        </div>
                      </div>
                    </b-card-body>
                  </b-card>
                </b-col>
                <b-col lg="12">
                  <b-card no-body class="card-block card-stretch card-height blog">
                    <b-card-body class="p-0">
                      <div class="d-flex align-items-center">
                        <div class="user-image mb-3">
                          <img class="avatar-80 rounded" src="@/assets/images/user/03.jpg" alt="#"
                            data-original-title="" title="" loading="lazy" />
                        </div>
                        <div class="ms-3">
                          <h5>Walter Hucko</h5>
                          <p>Web Designer</p>
                        </div>
                      </div>
                      <div class="blog-description">
                        <p>
                          There are many variations of passages of Lorem Ipsum
                          available, but the majority have suffered alteration
                          in some form, by injected humour, or randomised words
                          which don't look even slightly believable.
                        </p>
                        <div class="d-flex align-items-center justify-content-between mb-2 position-right-side">
                          <a href="#" class="comments d-flex align-items-center"><i
                              class="material-symbols-outlined pe-2 md-18 text-primary">
                              mode_comment </i>28 comments</a>
                          <span class="font-size-12 text-warning">
                            <i class="material-symbols-outlined md-18">star_half</i>
                            {{ "" }}
                            <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                            <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                            <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                            <i class="material-symbols-outlined md-18">star</i>
                          </span>
                        </div>
                      </div>
                    </b-card-body>
                  </b-card>
                </b-col>
                <b-col lg="12" class="ps-0 ps-md-5">
                  <b-card no-body class="card-block card-stretch card-height blog">
                    <b-card-body class="p-0">
                      <div class="d-flex align-items-center">
                        <div class="user-image mb-3">
                          <img class="avatar-80 rounded" src="@/assets/images/user/04.jpg" alt="#"
                            data-original-title="" title="" loading="lazy" />
                        </div>
                        <div class="ms-3">
                          <h5>Mark Walton</h5>
                          <p>Web Manager</p>
                        </div>
                      </div>
                      <div class="blog-description">
                        <p>
                          There are many variations of passages of Lorem Ipsum
                          available, but the majority have suffered
                          alteration.randomised words which don't look even
                          slightly believable variations of passages.
                        </p>
                        <div class="d-flex align-items-center justify-content-between mb-2 position-right-side">
                          <a href="#" class="comments d-flex align-items-center"><i
                              class="material-symbols-outlined pe-2 md-18 text-primary">
                              mode_comment </i>82 comments</a>
                          <span class="font-size-12 text-warning">
                            <i class="material-symbols-outlined md-18">star_half</i>
                            {{ "" }}
                            <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                            <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                            <i class="material-symbols-outlined md-18">star</i>{{ "" }}
                            <i class="material-symbols-outlined md-18">star</i>
                          </span>
                        </div>
                      </div>
                    </b-card-body>
                  </b-card>
                </b-col>
                <b-col lg="12">
                  <b-card no-body class="card-block card-stretch card-height blog">
                    <div class="card-header d-flex justify-content-between px-0 pt-0">
                      <div class="header-title">
                        <h4 class="card-title">Your Comment</h4>
                      </div>
                    </div>
                    <b-card-body class="p-0">
                      <form>
                        <div class="form-group">
                          <label for="email1" class="form-label">Email address:</label>
                          <input type="email" class="form-control" id="email1" />
                        </div>
                        <div class="form-group">
                          <label for="pwd" class="form-label">Password:</label>
                          <input type="password" class="form-control" id="pwd" />
                        </div>
                        <div class="form-group">
                          <label for="exampleFormControlTextarea1" class="form-label">Comment</label>
                          <textarea class="form-control" id="exampleFormControlTextarea1" rows="4"></textarea>
                        </div>
                        <div class="form-check mb-3 w-100">
                          <input class="form-check-input" type="checkbox" id="remember-box" value="option1" />
                          <label class="form-check-label" for="remember-box">Remember me</label>
                        </div>
                        <div class="d-flex align-items-center">
                          <button type="submit" class="btn btn-primary me-2">
                            Submit
                          </button>
                          <button type="submit" class="btn btn-danger">
                            Cancel
                          </button>
                        </div>
                      </form>
                    </b-card-body>
                  </b-card>
                </b-col>
              </b-row>
            </b-card-body>
          </b-card>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>
<script setup>
const blogPosts = [
  {
    date: "4 Weeks ago",
    title: "All the Lorem Ipsum generators",
    imageSrc: require("@/assets/images/blog/03.jpg"),
    borderBottom: "pb-3 border-bottom",
    mbclass: "mb-3",
  },
  {
    date: "3 Weeks ago",
    title: "All the Lorem Ipsum generators",
    imageSrc: require("@/assets/images/blog/04.jpg"),
    borderBottom: "pb-3 border-bottom",
    mbclass: "mb-3",
  },
  {
    date: "2 Weeks ago",
    title: "All the Lorem Ipsum generators",
    imageSrc: require("@/assets/images/blog/05.jpg"),
    borderBottom: "pb-3 border-bottom",
    mbclass: "mb-3",
  },
  {
    date: "1 Week ago",
    title: "All the Lorem Ipsum generators",
    imageSrc: require("@/assets/images/blog/06.jpg"),
    borderBottom: "pb-3 border-bottom",
    mbclass: "mb-3",
  },
  {
    date: "3 days ago",
    title: "All the Lorem Ipsum generators",
    imageSrc: require("@/assets/images/blog/07.jpg"),
    borderBottom: "pb-3 border-bottom",
    mbclass: "mb-3",
  },
  {
    date: "2 Days ago",
    title: "All the Lorem Ipsum generators",
    imageSrc: require("@/assets/images/blog/08.jpg"),
    borderBottom: "",
    mbclass: "",
  },
];
</script>
