<template>
  <div class="content-inner">
    <div class="container">
      <div class="d-grid gap-3 d-grid-template-1fr-19">
        <div class="card group-box mb-0">
          <div class="top-bg-image">
            <img
              src="@/assets/images/page-img/profile-bg1.jpg"
              class="img-fluid w-100"
              alt="group-bg"
            />
          </div>
          <div class="card-body text-center">
            <div class="group-icon">
              <img
                src="@/assets/images/page-img/gi-1.jpg"
                alt="profile-img"
                class="rounded-2 img-fluid avatar-90 border border-4"
              />
            </div>
            <div class="group-info mt-3 mb-2">
              <router-link :to="{ name: 'social.group-detail' }" class="h4"
                >Designer</router-link
              >
            </div>
            <div class="group-details pb-4 mb-4 border-bottom">
              <ul
                class="d-flex align-items-center justify-content-center list-inline m-0 p-0 gap-3"
              >
                <li>
                  <div class="d-flex align-items-center gap-1">
                    <span class="material-symbols-outlined font-size-18">
                      description
                    </span>
                    <span class="text-capitalize">1 posts</span>
                  </div>
                </li>
                <li>
                  <div class="d-flex align-items-center gap-1">
                    <span class="material-symbols-outlined font-size-18">
                      group
                    </span>
                    <span class="text-capitalize">Members</span>
                  </div>
                </li>
              </ul>
            </div>
            <div class="group-member mb-4">
              <div class="iq-media-group">
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/05.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
                {{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/06.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
                {{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/07.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
                {{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/08.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
                {{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/09.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
                {{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/10.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
              </div>
            </div>
            <button
              type="submit"
              class="btn btn-primary-subtle fw-semibold px-3"
            >
              Join Group
            </button>
          </div>
        </div>
        <div class="card group-box mb-0">
          <div class="top-bg-image">
            <img
              src="@/assets/images/page-img/profile-bg2.jpg"
              class="img-fluid w-100"
              alt="group-bg"
            />
          </div>
          <div class="card-body text-center">
            <div class="group-icon">
              <img
                src="@/assets/images/page-img/gi-2.jpg"
                alt="profile-img"
                class="rounded-2 img-fluid avatar-90 border border-4"
              />
            </div>
            <div class="group-info mt-3 mb-2">
              <router-link :to="{ name: 'social.group-detail' }" class="h4"
                >R & D</router-link
              >
            </div>
            <div class="group-details pb-4 mb-4 border-bottom">
              <ul
                class="d-flex align-items-center justify-content-center list-inline m-0 p-0 gap-3"
              >
                <li>
                  <div class="d-flex align-items-center gap-1">
                    <span class="material-symbols-outlined font-size-18">
                      description
                    </span>
                    <span class="text-capitalize">0 post</span>
                  </div>
                </li>
                <li>
                  <div class="d-flex align-items-center gap-1">
                    <span class="material-symbols-outlined font-size-18">
                      group
                    </span>
                    <span class="text-capitalize">Members 10</span>
                  </div>
                </li>
              </ul>
            </div>
            <div class="group-member mb-4">
              <div class="iq-media-group">
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/05.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
                {{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/06.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
                {{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/07.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
                {{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/08.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
                {{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/09.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
                {{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/10.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
              </div>
            </div>
            <div class="text-center">
              <button
                type="submit"
                class="btn btn-primary-subtle fw-semibold px-3"
              >
                Join Group
              </button>
            </div>
          </div>
        </div>
        <div class="card group-box mb-0">
          <div class="top-bg-image">
            <img
              src="@/assets/images/page-img/profile-bg3.jpg"
              class="img-fluid w-100"
              alt="group-bg"
            />
          </div>
          <div class="card-body text-center">
            <div class="group-icon">
              <img
                src="@/assets/images/page-img/gi-3.jpg"
                alt="profile-img"
                class="rounded-2 img-fluid avatar-90 border border-4"
              />
            </div>
            <div class="group-info mt-3 mb-2">
              <router-link :to="{ name: 'social.group-detail' }" class="h4"
                >Graphics</router-link
              >
            </div>
            <div class="group-details pb-4 mb-4 border-bottom">
              <ul
                class="d-flex align-items-center justify-content-center list-inline m-0 p-0 gap-3"
              >
                <li>
                  <div class="d-flex align-items-center gap-1">
                    <span class="material-symbols-outlined font-size-18">
                      description
                    </span>
                    <span class="text-capitalize">50+ posts</span>
                  </div>
                </li>
                <li>
                  <div class="d-flex align-items-center gap-1">
                    <span class="material-symbols-outlined font-size-18">
                      group
                    </span>
                    <span class="text-capitalize">Members 100+</span>
                  </div>
                </li>
              </ul>
            </div>
            <div class="group-member mb-4">
              <div class="iq-media-group">
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/05.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
                {{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/06.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
                {{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/07.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
                {{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/08.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
                {{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/09.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
                {{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/10.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
              </div>
            </div>
            <div class="text-center">
              <button
                type="submit"
                class="btn btn-danger-subtle fw-semibold px-3"
              >
                Leave Group
              </button>
            </div>
          </div>
        </div>
        <div class="card group-box mb-0">
          <div class="top-bg-image">
            <img
              src="@/assets/images/page-img/profile-bg4.jpg"
              class="img-fluid w-100"
              alt="group-bg"
            />
          </div>
          <div class="card-body text-center">
            <div class="group-icon">
              <img
                src="@/assets/images/page-img/gi-4.jpg"
                alt="profile-img"
                class="rounded-2 img-fluid avatar-90 border border-4"
              />
            </div>
            <div class="group-info mt-3 mb-2">
              <h4>
                <router-link :to="{ name: 'social.group-detail' }" class="h4"
                  >Developer</router-link
                >
              </h4>
            </div>
            <div class="group-details pb-4 mb-4 border-bottom">
              <ul
                class="d-flex align-items-center justify-content-center list-inline m-0 p-0 gap-3"
              >
                <li>
                  <div class="d-flex align-items-center gap-1">
                    <span class="material-symbols-outlined font-size-18">
                      description
                    </span>
                    <span class="text-capitalize">30 posts</span>
                  </div>
                </li>
                <li>
                  <div class="d-flex align-items-center gap-1">
                    <span class="material-symbols-outlined font-size-18">
                      group
                    </span>
                    <span class="text-capitalize">Members 48</span>
                  </div>
                </li>
              </ul>
            </div>
            <div class="group-member mb-4">
              <div class="iq-media-group">
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/05.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
                {{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/06.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
                {{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/07.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
                {{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/08.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
                {{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/09.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
                {{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/10.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
              </div>
            </div>
            <div class="text-center">
              <button
                type="submit"
                class="btn btn-primary-subtle fw-semibold px-3"
              >
                Join Group
              </button>
            </div>
          </div>
        </div>
        <div class="card group-box mb-0">
          <div class="top-bg-image">
            <img
              src="@/assets/images/page-img/profile-bg5.jpg"
              class="img-fluid w-100"
              alt="group-bg"
            />
          </div>
          <div class="card-body text-center">
            <div class="group-icon">
              <img
                src="@/assets/images/page-img/gi-5.jpg"
                alt="profile-img"
                class="rounded-2 img-fluid avatar-90 border border-4"
              />
            </div>
            <div class="group-info mt-3 mb-2">
              <router-link :to="{ name: 'social.group-detail' }" class="h4"
                >Tester</router-link
              >
            </div>
            <div class="group-details pb-4 mb-4 border-bottom">
              <ul
                class="d-flex align-items-center justify-content-center list-inline m-0 p-0 gap-3"
              >
                <li>
                  <div class="d-flex align-items-center gap-1">
                    <span class="material-symbols-outlined font-size-18">
                      description
                    </span>
                    <span class="text-capitalize">4 posts</span>
                  </div>
                </li>
                <li>
                  <div class="d-flex align-items-center gap-1">
                    <span class="material-symbols-outlined font-size-18">
                      group
                    </span>
                    <span class="text-capitalize">Members 24</span>
                  </div>
                </li>
              </ul>
            </div>
            <div class="group-member mb-4">
              <div class="iq-media-group">
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/05.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
                {{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/06.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
                {{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/07.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
                {{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/08.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
                {{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/09.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
                {{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/10.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
              </div>
            </div>
            <div class="text-center">
              <button
                type="submit"
                class="btn btn-success-subtle fw-semibold px-3"
              >
                Manage Group
              </button>
            </div>
          </div>
        </div>
        <div class="card group-box mb-0">
          <div class="top-bg-image">
            <img
              src="@/assets/images/page-img/profile-bg6.jpg"
              class="img-fluid w-100"
              alt="group-bg"
            />
          </div>
          <div class="card-body text-center">
            <div class="group-icon">
              <img
                src="@/assets/images/page-img/gi-6.jpg"
                alt="profile-img"
                class="rounded-2 img-fluid avatar-90 border border-4"
              />
            </div>
            <div class="group-info mt-3 mb-2">
              <router-link :to="{ name: 'social.group-detail' }" class="h4"
                >Events</router-link
              >
            </div>
            <div class="group-details pb-4 mb-4 border-bottom">
              <ul
                class="d-flex align-items-center justify-content-center list-inline m-0 p-0 gap-3"
              >
                <li>
                  <div class="d-flex align-items-center gap-1">
                    <span class="material-symbols-outlined font-size-18">
                      description
                    </span>
                    <span class="text-capitalize">8 posts</span>
                  </div>
                </li>
                <li>
                  <div class="d-flex align-items-center gap-1">
                    <span class="material-symbols-outlined font-size-18">
                      group
                    </span>
                    <span class="text-capitalize">Members 30</span>
                  </div>
                </li>
              </ul>
            </div>
            <div class="group-member mb-4">
              <div class="iq-media-group">
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/05.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
                {{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/06.jpg"
                    alt=""
                    loading="lazy"
                  /> </a
                >{{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/07.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
                {{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/08.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
                {{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/09.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
                {{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/10.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
              </div>
            </div>
            <div class="text-center">
              <button
                type="submit"
                class="btn btn-primary-subtle fw-semibold px-3"
              >
                Join Group
              </button>
            </div>
          </div>
        </div>
        <div class="card group-box">
          <div class="top-bg-image">
            <img
              src="@/assets/images/page-img/profile-bg7.jpg"
              class="img-fluid w-100"
              alt="group-bg"
            />
          </div>
          <div class="card-body text-center">
            <div class="group-icon">
              <img
                src="@/assets/images/page-img/gi-7.jpg"
                alt="profile-img"
                class="rounded-2 img-fluid avatar-90 border border-4"
              />
            </div>
            <div class="group-info mt-3 mb-2">
              <router-link :to="{ name: 'social.group-detail' }" class="h4"
                >Coder</router-link
              >
            </div>
            <div class="group-details pb-4 mb-4 border-bottom">
              <ul
                class="d-flex align-items-center justify-content-center list-inline m-0 p-0 gap-3"
              >
                <li>
                  <div class="d-flex align-items-center gap-1">
                    <span class="material-symbols-outlined font-size-18">
                      description
                    </span>
                    <span class="text-capitalize">19 posts</span>
                  </div>
                </li>
                <li>
                  <div class="d-flex align-items-center gap-1">
                    <span class="material-symbols-outlined font-size-18">
                      group
                    </span>
                    <span class="text-capitalize">Members 15</span>
                  </div>
                </li>
              </ul>
            </div>
            <div class="group-member mb-4">
              <div class="iq-media-group">
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/05.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
                {{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/06.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
                {{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/07.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
                {{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/08.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
                {{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/09.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
                {{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/10.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
              </div>
            </div>
            <div class="text-center">
              <button
                type="submit"
                class="btn btn-primary-subtle fw-semibold px-3"
              >
                Join Group
              </button>
            </div>
          </div>
        </div>
        <div class="card group-box">
          <div class="top-bg-image">
            <img
              src="@/assets/images/page-img/profile-bg9.jpg"
              class="img-fluid w-100"
              alt="group-bg"
            />
          </div>
          <div class="card-body text-center">
            <div class="group-icon">
              <img
                src="@/assets/images/page-img/gi-8.jpg"
                alt="profile-img"
                class="rounded-2 img-fluid avatar-90 border border-4"
              />
            </div>
            <div class="group-info mt-3 mb-2">
              <router-link :to="{ name: 'social.group-detail' }" class="h4"
                >Themes</router-link
              >
            </div>
            <div class="group-details pb-4 mb-4 border-bottom">
              <ul
                class="d-flex align-items-center justify-content-center list-inline m-0 p-0 gap-3"
              >
                <li>
                  <div class="d-flex align-items-center gap-1">
                    <span class="material-symbols-outlined font-size-18">
                      description
                    </span>
                    <span class="text-capitalize">27 posts</span>
                  </div>
                </li>
                <li>
                  <div class="d-flex align-items-center gap-1">
                    <span class="material-symbols-outlined font-size-18">
                      group
                    </span>
                    <span class="text-capitalize">Members 70</span>
                  </div>
                </li>
              </ul>
            </div>
            <div class="group-member mb-4">
              <div class="iq-media-group">
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/05.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
                {{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/06.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
                {{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/07.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
                {{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/08.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
                {{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/09.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
                {{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/10.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
              </div>
            </div>
            <div class="text-center">
              <button
                type="submit"
                class="btn btn-danger-subtle fw-semibold px-3"
              >
                Leave Group
              </button>
            </div>
          </div>
        </div>
        <div class="card group-box">
          <div class="top-bg-image">
            <img
              src="@/assets/images/page-img/profile-bg1.jpg"
              class="img-fluid w-100"
              alt="group-bg"
            />
          </div>
          <div class="card-body text-center">
            <div class="group-icon">
              <img
                src="@/assets/images/page-img/gi-9.jpg"
                alt="profile-img"
                class="rounded-2 img-fluid avatar-90 border border-4"
              />
            </div>
            <div class="group-info mt-3 mb-2">
              <router-link :to="{ name: 'social.group-detail' }" class="h4"
                >Review</router-link
              >
            </div>
            <div class="group-details pb-4 mb-4 border-bottom">
              <ul
                class="d-flex align-items-center justify-content-center list-inline m-0 p-0 gap-3"
              >
                <li>
                  <div class="d-flex align-items-center gap-1">
                    <span class="material-symbols-outlined font-size-18">
                      description
                    </span>
                    <span class="text-capitalize">32 posts</span>
                  </div>
                </li>
                <li>
                  <div class="d-flex align-items-center gap-1">
                    <span class="material-symbols-outlined font-size-18">
                      group
                    </span>
                    <span class="text-capitalize">Members 12</span>
                  </div>
                </li>
              </ul>
            </div>
            <div class="group-member mb-4">
              <div class="iq-media-group">
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/05.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
                {{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/06.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
                {{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/07.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
                {{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/08.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
                {{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/09.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
                {{ "" }}
                <a href="#" class="iq-media">
                  <img
                    class="img-fluid avatar-30 rounded-circle"
                    src="@/assets/images/user/10.jpg"
                    alt=""
                    loading="lazy"
                  />
                </a>
              </div>
            </div>
            <div class="text-center">
              <button
                type="submit"
                class="btn btn-success-subtle fw-semibold px-3"
              >
                Manage Group
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "Group",
  data() {
    return {
      groupInfo: [
        {
          backgroundimg: require("../../../assets/images/page-img/profile-bg1.jpg"),
          groupimg: require("../../../assets/images/page-img/gi-1.jpg"),
          title: "Designer",
          text: "Lorem Ipsum data",
          otherinfo: [
            {
              info: "post",
              value: "600",
            },
            {
              info: "Member",
              value: "320",
            },
            {
              info: "Visit",
              value: "1.2k",
            },
          ],
          groupMember: [
            require("../../../assets/images/user/05.jpg"),
            require("../../../assets/images/user/06.jpg"),
            require("../../../assets/images/user/07.jpg"),
            require("../../../assets/images/user/08.jpg"),
            require("../../../assets/images/user/09.jpg"),
          ],
        },
        {
          backgroundimg: require("../../../assets/images/page-img/profile-bg2.jpg"),
          groupimg: require("../../../assets/images/page-img/gi-2.jpg"),
          title: "R & D",
          text: "Lorem Ipsum data",
          otherinfo: [
            {
              info: "post",
              value: "300",
            },
            {
              info: "Member",
              value: "210",
            },
            {
              info: "Visit",
              value: "1.1k",
            },
          ],
          groupMember: [
            require("../../../assets/images/user/05.jpg"),
            require("../../../assets/images/user/06.jpg"),
            require("../../../assets/images/user/07.jpg"),
            require("../../../assets/images/user/08.jpg"),
            require("../../../assets/images/user/09.jpg"),
          ],
        },
        {
          backgroundimg: require("../../../assets/images/page-img/profile-bg3.jpg"),
          groupimg: require("../../../assets/images/page-img/gi-3.jpg"),
          title: "Graphics",
          text: "Lorem Ipsum data",
          otherinfo: [
            {
              info: "post",
              value: "320",
            },
            {
              info: "Member",
              value: "310",
            },
            {
              info: "Visit",
              value: "1.0k",
            },
          ],
          groupMember: [
            require("../../../assets/images/user/05.jpg"),
            require("../../../assets/images/user/06.jpg"),
            require("../../../assets/images/user/07.jpg"),
            require("../../../assets/images/user/08.jpg"),
            require("../../../assets/images/user/09.jpg"),
          ],
        },
        {
          backgroundimg: require("../../../assets/images/page-img/profile-bg4.jpg"),
          groupimg: require("../../../assets/images/page-img/gi-4.jpg"),
          title: "Developer",
          text: "Lorem Ipsum data",
          otherinfo: [
            {
              info: "post",
              value: "1000",
            },
            {
              info: "Member",
              value: "10000",
            },
            {
              info: "Visit",
              value: "1.5k",
            },
          ],
          groupMember: [
            require("../../../assets/images/user/05.jpg"),
            require("../../../assets/images/user/06.jpg"),
            require("../../../assets/images/user/07.jpg"),
            require("../../../assets/images/user/08.jpg"),
            require("../../../assets/images/user/09.jpg"),
          ],
        },
        {
          backgroundimg: require("../../../assets/images/page-img/profile-bg5.jpg"),
          groupimg: require("../../../assets/images/page-img/gi-5.jpg"),
          title: "Tester",
          text: "Lorem Ipsum data",
          otherinfo: [
            {
              info: "post",
              value: "600",
            },
            {
              info: "Member",
              value: "320",
            },
            {
              info: "Visit",
              value: "1.2k",
            },
          ],
          groupMember: [
            require("../../../assets/images/user/05.jpg"),
            require("../../../assets/images/user/06.jpg"),
            require("../../../assets/images/user/07.jpg"),
            require("../../../assets/images/user/08.jpg"),
            require("../../../assets/images/user/09.jpg"),
          ],
        },
        {
          backgroundimg: require("../../../assets/images/page-img/profile-bg6.jpg"),
          groupimg: require("../../../assets/images/page-img/gi-6.jpg"),
          title: "Events",
          text: "Lorem Ipsum data",
          otherinfo: [
            {
              info: "post",
              value: "200",
            },
            {
              info: "Member",
              value: "200",
            },
            {
              info: "Visit",
              value: "1.2k",
            },
          ],
          groupMember: [
            require("../../../assets/images/user/05.jpg"),
            require("../../../assets/images/user/06.jpg"),
            require("../../../assets/images/user/07.jpg"),
            require("../../../assets/images/user/08.jpg"),
            require("../../../assets/images/user/09.jpg"),
          ],
        },
        {
          backgroundimg: require("../../../assets/images/page-img/profile-bg7.jpg"),
          groupimg: require("../../../assets/images/page-img/gi-7.jpg"),
          title: "Coder",
          text: "Lorem Ipsum data",
          otherinfo: [
            {
              info: "post",
              value: "300",
            },
            {
              info: "Member",
              value: "200",
            },
            {
              info: "Visit",
              value: "1.4k",
            },
          ],
          groupMember: [
            require("../../../assets/images/user/05.jpg"),
            require("../../../assets/images/user/06.jpg"),
            require("../../../assets/images/user/07.jpg"),
            require("../../../assets/images/user/08.jpg"),
            require("../../../assets/images/user/09.jpg"),
          ],
        },
        {
          backgroundimg: require("../../../assets/images/page-img/profile-bg8.jpg"),
          groupimg: require("../../../assets/images/page-img/gi-8.jpg"),
          title: "Themes",
          text: "Lorem Ipsum data",
          otherinfo: [
            {
              info: "post",
              value: "800",
            },
            {
              info: "Member",
              value: "100",
            },
            {
              info: "Visit",
              value: "1.2k",
            },
          ],
          groupMember: [
            require("../../../assets/images/user/05.jpg"),
            require("../../../assets/images/user/06.jpg"),
            require("../../../assets/images/user/07.jpg"),
            require("../../../assets/images/user/08.jpg"),
            require("../../../assets/images/user/09.jpg"),
          ],
        },
        {
          backgroundimg: require("../../../assets/images/page-img/profile-bg9.jpg"),
          groupimg: require("../../../assets/images/page-img/gi-9.jpg"),
          title: "Review",
          text: "Lorem Ipsum data",
          otherinfo: [
            {
              info: "post",
              value: "1200",
            },
            {
              info: "Member",
              value: "1000",
            },
            {
              info: "Visit",
              value: "1.2k",
            },
          ],
          groupMember: [
            require("../../../assets/images/user/05.jpg"),
            require("../../../assets/images/user/06.jpg"),
            require("../../../assets/images/user/07.jpg"),
            require("../../../assets/images/user/08.jpg"),
            require("../../../assets/images/user/09.jpg"),
          ],
        },
      ],
    };
  },
};
</script>
