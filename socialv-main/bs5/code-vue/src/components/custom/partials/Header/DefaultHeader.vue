<template>
  <div class="iq-top-navbar border-bottom">
    <nav class="nav navbar navbar-expand-lg navbar-light iq-navbar p-lg-0">
      <div class="container-fluid navbar-inner">
        <div class="d-flex align-items-center pb-2 pb-lg-0 d-xl-none">
          <router-link
            :to="{ name: 'social.list' }"
            class="d-flex align-items-center iq-header-logo navbar-brand d-block d-xl-none"
          >
            <svg
              width="50"
              viewBox="0 0 24 24"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                fill-rule="evenodd"
                clip-rule="evenodd"
                d="M1.67733 9.50001L7.88976 20.2602C9.81426 23.5936 14.6255 23.5936 16.55 20.2602L22.7624 9.5C24.6869 6.16666 22.2813 2 18.4323 2H6.00746C2.15845 2 -0.247164 6.16668 1.67733 9.50001ZM14.818 19.2602C13.6633 21.2602 10.7765 21.2602 9.62181 19.2602L9.46165 18.9828L9.46597 18.7275C9.48329 17.7026 9.76288 16.6993 10.2781 15.8131L12.0767 12.7195L14.1092 16.2155C14.4957 16.8803 14.7508 17.6132 14.8607 18.3743L14.9544 19.0239L14.818 19.2602ZM16.4299 16.4683L19.3673 11.3806C18.7773 11.5172 18.172 11.5868 17.5629 11.5868H13.7316L15.8382 15.2102C16.0721 15.6125 16.2699 16.0335 16.4299 16.4683ZM20.9542 8.63193L21.0304 8.5C22.1851 6.5 20.7417 4 18.4323 4H17.8353L17.1846 4.56727C16.6902 4.99824 16.2698 5.50736 15.9402 6.07437L13.8981 9.58676H17.5629C18.4271 9.58676 19.281 9.40011 20.0663 9.03957L20.9542 8.63193ZM14.9554 4C14.6791 4.33499 14.4301 4.69248 14.2111 5.06912L12.0767 8.74038L10.0324 5.22419C9.77912 4.78855 9.48582 4.37881 9.15689 4H14.9554ZM6.15405 4H6.00746C3.69806 4 2.25468 6.50001 3.40938 8.50001L3.4915 8.64223L4.37838 9.04644C5.15962 9.40251 6.00817 9.58676 6.86672 9.58676H10.2553L8.30338 6.22943C7.9234 5.57587 7.42333 5.00001 6.8295 4.53215L6.15405 4ZM5.07407 11.3833L7.88909 16.2591C8.05955 15.7565 8.28025 15.2702 8.54905 14.8079L10.4218 11.5868H6.86672C6.26169 11.5868 5.66037 11.5181 5.07407 11.3833Z"
                fill="currentColor"
              />
            </svg>
            <h3 class="logo-title d-none d-sm-block" data-setting="app_name">
              {{ appName }}
            </h3>
          </router-link>
          <a
            class="sidebar-toggle"
            data-toggle="sidebar"
            data-active="true"
            href="#"
            @click="toggleSidebar()"
          >
            <div class="icon material-symbols-outlined iq-burger-menu">
              menu
            </div>
          </a>
        </div>
        <div class="d-flex align-items-center">
          <div
            class="d-flex align-items-center justify-content-between product-offcanvas"
          >
            <div
              class="offcanvas offcanvas-end shadow-none iq-product-menu-responsive d-none d-xl-block"
              tabindex="-1"
              id="offcanvasBottomNav"
            >
              <div class="offcanvas-body">
                <ul class="iq-nav-menu list-unstyled">
                  <li class="nav-item">
                    <router-link
                      :class="
                        checkActive('social.list')
                          ? 'active nav-link'
                          : 'nav-link'
                      "
                      :to="{ name: 'social.list' }"
                    >
                      <span class="nav-text">Home</span>
                    </router-link>
                  </li>
                  <li class="nav-item">
                    <a
                      class="nav-link menu-arrow justify-content-start"
                      data-bs-toggle="collapse"
                      href="#blogData"
                      role="button"
                      aria-expanded="false"
                      aria-controls="blogData"
                    >
                      <span class="nav-text">Blog</span>
                    </a>
                    <ul
                      class="iq-header-sub-menu list-unstyled collapse shadow"
                      id="blogData"
                    >
                      <li class="nav-item">
                        <router-link
                          :class="
                            checkActive('blog.blog-grid')
                              ? 'active nav-link'
                              : 'nav-link'
                          "
                          :to="{ name: 'blog.blog-grid' }"
                          >Blog Grid</router-link
                        >
                      </li>
                      <li class="nav-item">
                        <router-link
                          :class="
                            checkActive('blog.blog-list')
                              ? 'active nav-link'
                              : 'nav-link'
                          "
                          :to="{ name: 'blog.blog-list' }"
                          >Blog List</router-link
                        >
                      </li>
                      <li class="nav-item">
                        <router-link
                          :class="
                            checkActive('blog.blog-detail')
                              ? 'active nav-link'
                              : 'nav-link'
                          "
                          :to="{ name: 'blog.blog-detail' }"
                          >Blog Detail</router-link
                        >
                      </li>
                    </ul>
                  </li>
                  <li class="nav-item">
                    <a
                      class="nav-link menu-arrow justify-content-start"
                      data-bs-toggle="collapse"
                      href="#storeData"
                      role="button"
                      aria-expanded="false"
                      aria-controls="storeData"
                    >
                      <span class="nav-text">Store</span>
                    </a>
                    <ul
                      class="iq-header-sub-menu list-unstyled collapse shadow"
                      id="storeData"
                    >
                      <li class="nav-item">
                        <router-link
                          :class="
                            checkActive('store.category-grid')
                              ? 'active nav-link'
                              : 'nav-link'
                          "
                          :to="{ name: 'store.category-grid' }"
                          >Category Grid</router-link
                        >
                      </li>
                      <li class="nav-item">
                        <router-link
                          :class="
                            checkActive('store.category-list')
                              ? 'active nav-link'
                              : 'nav-link'
                          "
                          :to="{ name: 'store.category-list' }"
                          >Category List</router-link
                        >
                      </li>
                      <li class="nav-item">
                        <router-link
                          :class="
                            checkActive('store.store-detail')
                              ? 'active nav-link'
                              : 'nav-link'
                          "
                          :to="{ name: 'store.store-detail' }"
                          >Store Detail</router-link
                        >
                      </li>
                      <li class="nav-item">
                        <router-link
                          :class="
                            checkActive('store.product-detail')
                              ? 'active nav-link'
                              : 'nav-link'
                          "
                          :to="{ name: 'store.product-detail' }"
                          >Product Detail</router-link
                        >
                      </li>

                      <li class="nav-item">
                        <router-link
                          :class="
                            checkActive('store.checkout')
                              ? 'active nav-link'
                              : 'nav-link'
                          "
                          :to="{ name: 'store.checkout' }"
                          >Checkout</router-link
                        >
                      </li>
                    </ul>
                  </li>
                </ul>
              </div>
            </div>
          </div>
          <div class="iq-search-bar device-search position-relative d-none d-lg-block">
            <form action="#" class="searchbox open-modal-search" @click="toggleSearchModal()">
              <a class="search-link" href="#">
                <svg width="16" height="17" viewBox="0 0 16 17" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <circle cx="7.82491" cy="7.82495" r="6.74142" stroke="currentColor" stroke-width="1.5"
                    stroke-linecap="round" stroke-linejoin="round" />
                  <path d="M12.5137 12.8638L15.1567 15.5" stroke="currentColor" stroke-width="1.5"
                    stroke-linecap="round" stroke-linejoin="round" />
                </svg>
              </a>
              <input type="text" class="text search-input form-control bg-light-subtle"
                placeholder="Search for people or groups..."  />
            </form>

            <!--  modal full screen modal -->
            <div id="search-modal" class="search-modal-custom" :class="className">

              <div class="search-modal-content">
                <div class="px-3 py-2">
                  <div class="d-lg-none w-100">
                    <form action="#" class="searchbox">
                      <a class="search-link" href="/">
                        <svg width="16" height="17" viewBox="0 0 16 17" fill="none" xmlns="http://www.w3.org/2000/svg">
                          <circle cx="7.82491" cy="7.82495" r="6.74142" stroke="currentColor" stroke-width="1.5"
                            stroke-linecap="round" stroke-linejoin="round"></circle>
                          <path d="M12.5137 12.8638L15.1567 15.5" stroke="currentColor" stroke-width="1.5"
                            stroke-linecap="round" stroke-linejoin="round"></path>
                        </svg>
                      </a>
                      <input type="text" class="text search-input bg-primary-subtle" placeholder="Search here...">
                    </form>
                  </div>
                  <div class="d-none d-lg-flex align-items-center justify-content-between w-100">
                    <h4 class="modal-title" id="exampleModalFullscreenLabel">Recent</h4>
                    <a href="/" class="text-dark">Clear All</a>
                  </div>
                </div>
                <div class="p-0">
                  <div class="item-header-scroll">
                    <div class="search-modal-body">
                      <div class="d-flex d-lg-none align-items-center justify-content-between w-100 p-3 pb-0">
                        <h5 class="modal-title h4" id="exampleModalFullscreenLabel">Recent</h5>
                        <a href="#" class="text-dark">Clear All</a>
                      </div>
                      <div class="d-flex align-items-center search-hover py-2 px-3">
                        <div class="flex-shrink-0">
                          <img src="@/assets/images/page-img/19.jpg"
                            class="align-self-center img-fluid avatar-50 rounded-pill" alt="#">
                        </div>
                        <div class="d-flex ms-3 w-100 justify-content-between">
                          <div class="d-flex flex-column">
                            <div><a href="#" class="h6">Paige Turner</a><span class="profile-status-online"></span>
                            </div>
                            <span class="mb-0">Paige001</span>
                          </div>
                          <a href="#" class="material-symbols-outlined text-dark font-size-16">close</a>
                        </div>
                      </div>
                      <div class="d-flex align-items-center search-hover py-2 px-3">
                        <div class="flex-shrink-0">
                          <img src="@/assets/images/page-img/18.jpg"
                            class="align-self-center img-fluid avatar-50 rounded-pill" alt="#">
                        </div>
                        <div class="d-flex ms-3 w-100 justify-content-between">
                          <div class="d-flex flex-column">
                            <div><a href="#" class="h6">Monty Carlo</a><span class="profile-status-online"></span>
                            </div>
                            <span class="mb-0">Carlo.m</span>
                          </div>
                          <a href="#" class="material-symbols-outlined text-dark font-size-16">close</a>
                        </div>
                      </div>
                      <div class="d-flex align-items-center search-hover py-2 px-3">
                        <div class="flex-shrink-0">
                          <img src="@/assets/images/page-img/20.jpg"
                            class="align-self-center img-fluid avatar-50 rounded-pill" alt="#">
                        </div>
                        <div class="d-flex ms-3 w-100 justify-content-between">
                          <div class="d-flex flex-column">
                            <div><a href="#" class="h6">Paul Molive</a><span class="profile-status-offline"></span>
                            </div>
                            <span class="mb-0">Paul.45</span>
                          </div>
                          <a href="#" class="material-symbols-outlined text-dark font-size-16">close</a>
                        </div>
                      </div>
                      <div class="py-2 px-3">
                        <h5 class="modal-title " id="exampleModalFullscreenLabel">Suggestion</h5>
                      </div>
                      <div class="d-flex align-items-center search-hover py-2 px-3">
                        <div class="flex-shrink-0">
                          <img src="@/assets/images/page-img/19.jpg"
                            class="align-self-center img-fluid avatar-50 rounded-pill" alt="#">
                        </div>
                        <div class="d-flex ms-3 w-100 justify-content-between">
                          <div class="d-flex flex-column">
                            <div><a href="#" class="h6">Annette Black</a>
                            </div>
                            <span class="mb-0">Followed by Jerome_bell + 2 more</span>
                          </div>
                          <a href="#" class="material-symbols-outlined text-dark font-size-16">close</a>
                        </div>
                      </div>
                      <div class="d-flex align-items-center search-hover py-2 px-3">
                        <div class="flex-shrink-0">
                          <img src="@/assets/images/page-img/18.jpg"
                            class="align-self-center img-fluid avatar-50 rounded-pill" alt="#">
                        </div>
                        <div class="d-flex ms-3 w-100 justify-content-between">
                          <div class="d-flex flex-column">
                            <div><a href="#" class="h6">Ellyse Perry</a>
                            </div>
                            <span class="mb-0">Followed by _@rina</span>
                          </div>
                          <a href="#" class="material-symbols-outlined text-dark font-size-16">close</a>
                        </div>
                      </div>
                      <div class="d-flex align-items-center search-hover py-2 px-3">
                        <div class="flex-shrink-0">
                          <img src="@/assets/images/page-img/20.jpg"
                            class="align-self-center img-fluid avatar-50 rounded-pill" alt="#">
                        </div>
                        <div class="d-flex ms-3 w-100 justify-content-between">
                          <div class="d-flex flex-column">
                            <div><a href="#" class="h6">Pete Sariya</a>
                            </div>
                            <span class="mb-0">Followed by chris_18 + 5 more</span>
                          </div>
                          <a href="#" class="material-symbols-outlined text-dark font-size-16">close</a>
                        </div>
                      </div>
                      <div class="d-flex align-items-center search-hover py-2 px-3">
                        <div class="flex-shrink-0">
                          <img src="@/assets/images/page-img/20.jpg"
                            class="align-self-center img-fluid avatar-50 rounded-pill" alt="#">
                        </div>
                        <div class="d-flex ms-3 w-100 justify-content-between">
                          <div class="d-flex flex-column">
                            <div><a href="#" class="h6">Aman Verma</a>
                            </div>
                            <span class="mb-0">Followed by chris_18 + 5 more</span>
                          </div>
                          <a href="#" class="material-symbols-outlined text-dark font-size-16">close</a>
                        </div>
                      </div>
                      <!-- Other similar blocks omitted for brevity -->
                    </div>
                  </div>
                </div>
              </div>
            </div>

          </div>

        </div>

        <ul class="navbar-nav navbar-list">
          <li class="nav-item dropdown">
            <a
              href="#"
              class="dropdown-toggle d-flex align-items-center"
              id="mail-drop"
              data-bs-toggle="dropdown"
              aria-haspopup="true"
              aria-expanded="false"
            >
              <span class="material-symbols-outlined position-relative"
                >shopping_bag
                <span class="bg-primary text-white shopping-badge">3</span>
              </span>
              <span class="mobile-text d-none ms-3">Shopping Cart</span>
            </a>
            <div
              class="sub-drop dropdown-menu header-notification"
              aria-labelledby="mail-drop"
            >
              <div class="card shadow m-0">
                <div
                  class="card-header d-flex justify-content-between px-0 pb-4 mx-5 border-bottom"
                >
                  <div class="header-title">
                    <h5 class="fw-semibold">Shopping Cart</h5>
                  </div>
                </div>
                <div class="card-body p-0 rounded-0">
                  <div class="item-header-scroll">
                    <a href="#" class="text-body">
                      <div
                        class="thread d-flex justify-content-between rounded-0"
                      >
                        <div>
                          <img
                            class="avatar-45 rounded align-top"
                            src="@/assets/images/store/06.jpg"
                            alt=""
                            loading="lazy"
                          />{{ "" }}
                          <div class="ms-3 d-inline-block">
                            <h6 class="font-size-14">Casual Shoe</h6>
                            <span class="font-size-14 fw-semibold">$75.00</span>
                          </div>
                        </div>
                        <span class="material-symbols-outlined">close</span>
                      </div>
                    </a>
                    <a href="#" class="text-body">
                      <div
                        class="thread d-flex justify-content-between rounded-0"
                      >
                        <div>
                          <img
                            class="avatar-45 rounded align-top"
                            src="@/assets/images/store/02.jpg"
                            alt=""
                            loading="lazy"
                          />{{ "" }}
                          <div class="ms-3 d-inline-block">
                            <h6 class="font-size-14">Harsh Reality book</h6>
                            <span class="font-size-14 fw-semibold">$25.00</span>
                          </div>
                        </div>
                        <span class="material-symbols-outlined">close</span>
                      </div>
                    </a>
                    <a href="#" class="text-body">
                      <div
                        class="thread d-flex justify-content-between rounded-0"
                      >
                        <div>
                          <img
                            class="avatar-45 rounded align-top"
                            src="@/assets/images/store/01.jpg"
                            alt=""
                            loading="lazy"
                          />{{ "" }}
                          <div class="ms-3 d-inline-block">
                            <h6 class="font-size-14">The Raze night book</h6>
                            <span class="font-size-14 fw-semibold">$15.00</span>
                          </div>
                        </div>
                        <span class="material-symbols-outlined">close</span>
                      </div>
                    </a>
                  </div>
                  <div class="m-5 mt-4">
                    <div
                      class="d-flex align-items-center justify-content-between mb-3"
                    >
                      <h6 class="font-size-14 fw-bolder">Subtotal:</h6>
                      <span class="font-size-14 fw-semibold text-primary"
                        >$115.00</span
                      >
                    </div>
                    <button type="button" class="btn btn-primary fw-500 w-100">
                      View All Products
                    </button>
                  </div>
                </div>
              </div>
            </div>
          </li>
          <li class="nav-item d-lg-none">
            <div class="iq-search-bar device-search position-relative">
              <form
                action="#"
                class="searchbox"
                data-bs-toggle="modal"
                data-bs-target="#exampleModalFullscreenSm"
              >
                <a class="search-link d-none d-lg-block" href="#">
                  <span class="material-symbols-outlined">search</span>
                </a>
                <input
                  type="text"
                  class="text search-input form-control bg-soft-primary d-none d-lg-block"
                  placeholder="Search here..."
                />
                <div
                  class="d-lg-none d-flex text-body"
                  @click="toggleSearchModal()"
                >
                  <svg
                    width="16"
                    height="17"
                    viewBox="0 0 16 17"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <circle
                      cx="7.82491"
                      cy="7.82495"
                      r="6.74142"
                      stroke="currentColor"
                      stroke-width="1.5"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                    ></circle>
                    <path
                      d="M12.5137 12.8638L15.1567 15.5"
                      stroke="currentColor"
                      stroke-width="1.5"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                    ></path>
                  </svg>
                </div>
              </form>
              <!--  modal full screen modal -->
              <div
                class="modal fade search-modal"
                id="exampleModalFullscreenSm"
                aria-labelledby="exampleModalFullscreenSmLabel"
                aria-hidden="true"
              >
                <div class="modal-dialog modal-fullscreen-lg-down">
                  <div class="modal-content">
                    <div class="modal-header py-2">
                      <div
                        class="d-flex align-items-center justify-content-between d-lg-none w-100"
                      >
                        <form
                          action="#"
                          class="searchbox w-50"
                          data-bs-toggle="modal"
                          data-bs-target="#exampleModalFullscreenSm"
                        >
                          <a class="search-link" href="#">
                            <span class="material-symbols-outlined"
                              >search</span
                            >
                          </a>
                          <input
                            type="text"
                            class="text search-input form-control bg-soft-primary"
                            placeholder="Search here..."
                          />
                        </form>
                        <a
                          href="#"
                          class="material-symbols-outlined text-dark"
                          data-bs-dismiss="modal"
                          >close</a
                        >
                      </div>
                      <div
                        class="d-none d-lg-flex align-items-center justify-content-between w-100"
                      >
                        <h4
                          class="modal-title"
                          id="exampleModalFullscreenLabel"
                        >
                          Recent
                        </h4>
                        <a class="text-dark" href="#">Clear All</a>
                      </div>
                    </div>
                    <div class="modal-body p-0">
                      <div
                        class="d-flex d-lg-none align-items-center justify-content-between w-100 p-3 pb-0"
                      >
                        <h5
                          class="modal-title h4"
                          id="exampleModalFullscreenLabel"
                        >
                          Recent
                        </h5>
                        <a href="#" class="text-dark">Clear All</a>
                      </div>
                      <div
                        class="d-flex align-items-center border-bottom search-hover py-2 px-3"
                      >
                        <div class="flex-shrink-0">
                          <img
                            src="@/assets/images/page-img/19.jpg"
                            class="align-self-center img-fluid avatar-50 rounded-pill"
                            alt="#"
                          />
                        </div>
                        <div class="d-flex flex-column ms-3">
                          <a href="#" class="h5">Paige Turner</a>
                          <span>Paige001</span>
                        </div>
                        <div class="d-flex align-items-center ms-auto">
                          <a href="#" class="me-3 d-flex align-items-center"
                            ><small>Follow</small>
                          </a>
                          <a
                            href="#"
                            class="material-symbols-outlined text-dark"
                            >close</a
                          >
                        </div>
                      </div>
                      <div
                        class="d-flex align-items-center border-bottom search-hover py-2 px-3"
                      >
                        <div class="flex-shrink-0">
                          <img
                            src="@/assets/images/page-img/18.jpg"
                            class="align-self-center img-fluid avatar-50 rounded-pill"
                            alt="#"
                          />
                        </div>
                        <div class="d-flex flex-column ms-3">
                          <a href="#" class="h5">Monty Carlo</a>
                          <span>Carlo.m</span>
                        </div>
                        <div class="d-flex align-items-center ms-auto">
                          <a href="#" class="me-3 d-flex align-items-center"
                            ><small>Unfollow</small>
                          </a>
                          <a
                            href="#"
                            class="material-symbols-outlined text-dark"
                            >close</a
                          >
                        </div>
                      </div>
                      <div
                        class="d-flex align-items-center search-hover py-2 px-3 border-bottom"
                      >
                        <div class="flex-shrink-0">
                          <img
                            src="@/assets/images/page-img/20.jpg"
                            class="align-self-center img-fluid avatar-50 rounded-pill"
                            alt="#"
                          />
                        </div>
                        <div class="d-flex flex-column ms-3">
                          <a href="#" class="h5">Paul Molive</a>
                          <span>Paul.45</span>
                        </div>
                        <div class="d-flex align-items-center ms-auto">
                          <a href="#" class="me-3 d-flex align-items-center"
                            ><small>Request</small>
                          </a>
                          <a
                            href="#"
                            class="material-symbols-outlined text-dark"
                            >close</a
                          >
                        </div>
                      </div>
                      <div class="">
                        <h4 class="px-3 py-0">Suggestions</h4>
                        <div class="suggestion-card px-3 d-flex">
                          <div class="text-center story">
                            <div class="story-profile">
                              <img
                                src="@/assets/images/page-img/20.jpg"
                                class="avatar-50 rounded-pill"
                                alt="#"
                              />
                              <a
                                href="#"
                                class="h6 mt-0 mt-lg-2 ms-3 ms-lg-0 text-ellipsis short-2 small"
                                >Ammy Paul</a
                              >
                            </div>
                            <a
                              href="#"
                              class="d-lg-none align-items-center d-flex"
                              ><small>Follow</small>
                            </a>
                          </div>
                          <div class="text-center story">
                            <div class="story-profile">
                              <img
                                src="@/assets/images/page-img/21.jpg"
                                class="avatar-50 rounded-pill"
                                alt="#"
                              />
                              <a
                                href="#"
                                class="h6 mt-0 mt-lg-2 ms-3 ms-lg-0 text-ellipsis short-2 small"
                                >Roger Carlo</a
                              >
                            </div>
                            <a
                              href="#"
                              class="d-lg-none align-items-center d-flex"
                              ><small>Unfollow</small>
                            </a>
                          </div>
                          <div class="text-center story">
                            <div class="story-profile">
                              <img
                                src="@/assets/images/page-img/22.jpg"
                                class="avatar-50 rounded-pill"
                                alt="#"
                              />
                              <a
                                href="#"
                                class="h6 mt-0 mt-lg-2 ms-3 ms-lg-0 text-ellipsis short-2 small"
                                >Justin Molive</a
                              >
                            </div>
                            <a
                              href="#"
                              class="d-lg-none align-items-center d-flex"
                              ><small>Follow</small>
                            </a>
                          </div>
                          <div class="text-center story">
                            <div class="story-profile">
                              <img
                                src="@/assets/images/page-img/23.jpg"
                                class="avatar-50 rounded-pill"
                                alt="#"
                              />
                              <a
                                href="#"
                                class="h6 mt-0 mt-lg-2 ms-3 ms-lg-0 text-ellipsis short-2 small"
                                >Roy Fisher</a
                              >
                            </div>
                            <a
                              href="#"
                              class="d-lg-none align-items-center d-flex"
                              ><small>Request</small>
                            </a>
                          </div>
                          <div class="text-center story">
                            <div class="story-profile">
                              <img
                                src="@/assets/images/page-img/24.jpg"
                                class="avatar-50 rounded-pill"
                                alt="#"
                              />
                              <a
                                href="#"
                                class="h6 mt-0 mt-lg-2 ms-3 ms-lg-0 text-ellipsis short-2 small"
                                >Johan Carlo</a
                              >
                            </div>
                            <a
                              href="#"
                              class="d-lg-none align-items-center d-flex"
                              ><small>Follow</small>
                            </a>
                          </div>
                          <div class="text-center story">
                            <div class="story-profile">
                              <img
                                src="@/assets/images/page-img/09.jpg"
                                class="avatar-50 rounded-pill"
                                alt="#"
                              />
                              <a
                                href="#"
                                class="h6 mt-0 mt-lg-2 ms-3 ms-lg-0 text-ellipsis short-2 small"
                                >Medra Miles</a
                              >
                            </div>
                            <a
                              href="#"
                              class="d-lg-none align-items-center d-flex"
                              ><small>Unfollow</small>
                            </a>
                          </div>
                          <div class="text-center story">
                            <div class="story-profile">
                              <img
                                src="@/assets/images/page-img/03.jpg"
                                class="avatar-50 rounded-pill"
                                alt="#"
                              />
                              <a
                                href="#"
                                class="h6 mt-0 mt-lg-2 ms-3 ms-lg-0 text-ellipsis short-2 small"
                                >Aohan Paul</a
                              >
                            </div>
                            <a
                              href="#"
                              class="d-lg-none align-items-center d-flex"
                              ><small>Request</small>
                            </a>
                          </div>
                          <div class="text-center story">
                            <div class="story-profile">
                              <img
                                src="@/assets/images/page-img/02.jpg"
                                class="avatar-50 rounded-pill"
                                alt="#"
                              />
                              <a
                                href="#"
                                class="h6 mt-0 mt-lg-2 ms-3 ms-lg-0 text-ellipsis short-2 small"
                                >Rokni Joy</a
                              >
                            </div>
                            <a
                              href="#"
                              class="d-lg-none align-items-center d-flex"
                              ><small>Follow</small>
                            </a>
                          </div>
                          <div class="text-center story">
                            <div class="story-profile">
                              <img
                                src="@/assets/images/page-img/09.jpg"
                                class="avatar-50 rounded-pill"
                                alt="#"
                              />
                              <a
                                href="#"
                                class="h6 mt-0 mt-lg-2 ms-3 ms-lg-0 text-ellipsis short-2 small"
                                >Sepid Ryan</a
                              >
                            </div>
                            <a
                              href="#"
                              class="d-lg-none align-items-center d-flex"
                              ><small>Unfollow</small>
                            </a>
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </li>
          <li class="nav-item dropdown">
            <a
              href="#"
              class="dropdown-toggle d-flex align-items-center"
              id="group-drop"
              data-bs-toggle="dropdown"
              aria-haspopup="true"
              aria-expanded="false"
            >
              <span class="material-symbols-outlined">group</span>
            </a>
            <div
              class="sub-drop sub-drop-large dropdown-menu"
              aria-labelledby="group-drop"
            >
              <div class="card shadow m-0">
                <div
                  class="card-header d-flex justify-content-between px-0 pb-4 mx-5 border-bottom"
                >
                  <div class="header-title">
                    <h5 class="fw-semibold">Friend Request</h5>
                  </div>
                </div>
                <div class="card-body">
                  <div class="item-header-scroll">
                    <div class="iq-friend-request">
                      <div
                        class="iq-sub-card-big d-flex align-items-center justify-content-between mb-4"
                      >
                        <div class="d-flex align-items-center">
                          <img
                            class="avatar-40 rounded-pill"
                            src="@/assets/images/user/01.jpg"
                            alt=""
                            loading="lazy"
                          />
                          <div class="ms-3">
                            <h6 class="mb-0">Jaques Amole</h6>
                            <p class="mb-0">40 friends</p>
                          </div>
                        </div>
                        <div class="d-flex align-items-center">
                          <a
                            href="#"
                            class="me-2 rounded bg-primary-subtle border-0 d-inline-block px-1"
                          >
                            <span
                              class="material-symbols-outlined font-size-18 align-text-bottom"
                            >
                              add
                            </span>
                          </a>
                          <a
                            href="#"
                            class="me-3 rounded bg-danger-subtle border-0 d-inline-block px-1"
                          >
                            <span
                              class="material-symbols-outlined font-size-18 align-text-bottom"
                            >
                              close
                            </span>
                          </a>
                        </div>
                      </div>
                    </div>
                    <div class="iq-friend-request">
                      <div
                        class="iq-sub-card-big d-flex align-items-center justify-content-between mb-4"
                      >
                        <div class="d-flex align-items-center">
                          <img
                            class="avatar-40 rounded-pill"
                            src="@/assets/images/user/02.jpg"
                            alt=""
                            loading="lazy"
                          />
                          <div class="ms-3">
                            <h6 class="mb-0">Lucy Tania</h6>
                            <p class="mb-0">12 friends</p>
                          </div>
                        </div>
                        <div class="d-flex align-items-center">
                          <a
                            href="#"
                            class="me-2 rounded bg-primary-subtle border-0 d-inline-block px-1"
                          >
                            <span
                              class="material-symbols-outlined font-size-18 align-text-bottom"
                            >
                              add
                            </span>
                          </a>
                          <a
                            href="#"
                            class="me-3 rounded bg-danger-subtle border-0 d-inline-block px-1"
                          >
                            <span
                              class="material-symbols-outlined font-size-18 align-text-bottom"
                            >
                              close
                            </span>
                          </a>
                        </div>
                      </div>
                    </div>
                    <div class="iq-friend-request">
                      <div
                        class="iq-sub-card-big d-flex align-items-center justify-content-between mb-4"
                      >
                        <div class="d-flex align-items-center">
                          <img
                            class="avatar-40 rounded-pill"
                            src="@/assets/images/user/03.jpg"
                            alt=""
                            loading="lazy"
                          />
                          <div class="ms-3">
                            <h6 class="mb-0">Manny Petty</h6>
                            <p class="mb-0">3 friends</p>
                          </div>
                        </div>
                        <div class="d-flex align-items-center">
                          <a
                            href="#"
                            class="me-2 rounded bg-primary-subtle border-0 d-inline-block px-1"
                          >
                            <span
                              class="material-symbols-outlined font-size-18 align-text-bottom"
                            >
                              add
                            </span>
                          </a>
                          <a
                            href="#"
                            class="me-3 rounded bg-danger-subtle border-0 d-inline-block px-1"
                          >
                            <span
                              class="material-symbols-outlined font-size-18 align-text-bottom"
                            >
                              close
                            </span>
                          </a>
                        </div>
                      </div>
                    </div>
                    <div class="iq-friend-request">
                      <div
                        class="iq-sub-card-big d-flex align-items-center justify-content-between"
                      >
                        <div class="d-flex align-items-center">
                          <img
                            class="avatar-40 rounded-pill"
                            src="@/assets/images/user/04.jpg"
                            alt=""
                            loading="lazy"
                          />
                          <div class="ms-3">
                            <h6 class="mb-0">Marsha Mello</h6>
                            <p class="mb-0">15 friends</p>
                          </div>
                        </div>
                        <div class="d-flex align-items-center">
                          <a
                            href="#"
                            class="me-2 rounded bg-primary-subtle border-0 d-inline-block px-1"
                          >
                            <span
                              class="material-symbols-outlined font-size-18 align-text-bottom"
                            >
                              add
                            </span>
                          </a>
                          <a
                            href="#"
                            class="me-3 rounded bg-danger-subtle border-0 d-inline-block px-1"
                          >
                            <span
                              class="material-symbols-outlined font-size-18 align-text-bottom"
                            >
                              close
                            </span>
                          </a>
                        </div>
                      </div>
                    </div>
                  </div>
                  <div class="text-center">
                    <button type="button" class="btn btn-primary fw-500 mt-4">
                      View More Request
                    </button>
                  </div>
                </div>
              </div>
            </div>
          </li>

          <li class="nav-item dropdown">
            <a
              href="#"
              class="dropdown-toggle d-flex align-items-center"
              id="mail-drop"
              data-bs-toggle="dropdown"
              aria-haspopup="true"
              aria-expanded="false"
            >
              <i class="material-symbols-outlined">mail</i>
              <span class="mobile-text d-none ms-3">Message</span>
            </a>
            <div
              class="sub-drop dropdown-menu header-notification"
              aria-labelledby="mail-drop"
            >
              <div class="card shadow m-0">
                <div
                  class="card-header d-flex justify-content-between px-0 pb-4 mx-5 border-bottom"
                >
                  <div class="header-title">
                    <h5 class="fw-semibold">All Message</h5>
                  </div>
                </div>
                <div class="card-body p-0">
                  <div class="item-header-scroll">
                    <a href="#">
                      <div
                        class="thread d-flex align-items-center justify-content-between rounded-0"
                      >
                        <div>
                          <img
                            class="avatar-40 rounded-pill align-top"
                            src="@/assets/images/user/01.jpg"
                            alt=""
                            loading="lazy"
                          />{{ "" }}
                          <div class="ms-3 d-inline-block">
                            <h6>Bni Emma Watson</h6>
                            <small class="fw-500 text-body"
                              >Hello how are you?</small
                            >
                          </div>
                        </div>
                        <small class="text-body">1 hr. ago</small>
                      </div>
                    </a>
                    <a href="#">
                      <div
                        class="thread d-flex align-items-center justify-content-between rounded-0"
                      >
                        <div>
                          <img
                            class="avatar-40 rounded-pill align-top"
                            src="@/assets/images/user/02.jpg"
                            alt=""
                            loading="lazy"
                          />{{ "" }}
                          <div class="ms-3 d-inline-block">
                            <h6>John Travolta</h6>
                            <small class="fw-500 text-body"
                              >Yes, same here. Bye.</small
                            >
                          </div>
                        </div>
                        <small class="text-body">4 hr. ago</small>
                      </div>
                    </a>
                    <a href="#">
                      <div
                        class="thread d-flex align-items-center justify-content-between rounded-0"
                      >
                        <div>
                          <img
                            class="avatar-40 rounded-pill align-top"
                            src="@/assets/images/user/03.jpg"
                            alt=""
                            loading="lazy"
                          />{{ "" }}
                          <div class="ms-3 d-inline-block">
                            <h6>Maya Didas</h6>
                            <small class="fw-500 text-body"
                              >that’s great, see you soon</small
                            >
                          </div>
                        </div>
                        <small class="text-body">9 hr. ago</small>
                      </div>
                    </a>
                    <a href="#">
                      <div
                        class="thread d-flex align-items-center justify-content-between rounded-0"
                      >
                        <div>
                          <img
                            class="avatar-40 rounded-pill align-top"
                            src="@/assets/images/user/07.jpg"
                            alt=""
                            loading="lazy"
                          />{{ "" }}
                          <div class="ms-3 d-inline-block">
                            <h6>Paige Turner</h6>
                            <small class="fw-500 text-body"
                              >Yes, let’s go.</small
                            >
                          </div>
                        </div>
                        <small class="text-body">1 yr. ago</small>
                      </div>
                    </a>
                  </div>
                  <div class="m-5 mt-4">
                    <button type="button" class="btn btn-primary fw-500 w-100">
                      View All Messages
                    </button>
                  </div>
                </div>
              </div>
            </div>
          </li>
          <li class="nav-item dropdown">
            <a
              href="#"
              class="search-toggle dropdown-toggle d-flex align-items-center"
              id="notification-drop"
              data-bs-toggle="dropdown"
            >
              <span class="material-symbols-outlined position-relative"
                >notifications
                <span class="bg-primary text-white notification-badge"></span>
              </span>
            </a>

            <div
              class="sub-drop dropdown-menu header-notification"
              aria-labelledby="notification-drop"
            >
              <div class="card m-0 shadow">
                <div
                  class="card-header d-flex justify-content-between px-0 pb-4 mx-5 border-bottom"
                >
                  <div class="header-title">
                    <h5 class="fw-semibold">Notifications</h5>
                  </div>
                  <h6 class="material-symbols-outlined">settings</h6>
                </div>
                <div class="card-body">
                  <div class="item-header-scroll">
                    <a href="#">
                      <div class="d-flex gap-3 mb-4">
                        <img
                          class="avatar-32 rounded-pill"
                          src="@/assets/images/user/01.jpg"
                          alt=""
                        />
                        <div>
                          <h6 class="font-size-14">
                            Pete Sariya
                            <span class="text-body fw-normal">voted for</span>
                            combination of colors from your brand palette
                          </h6>
                          <small class="text-body fw-500">1 month ago</small>
                        </div>
                      </div>
                    </a>
                    <a href="#">
                      <div class="d-flex gap-3 mb-4">
                        <img
                          class="avatar-32 rounded-pill"
                          src="@/assets/images/user/02.jpg"
                          alt=""
                          loading="lazy"
                        />
                        <div>
                          <h6 class="font-size-14">
                            Dima Davydov
                            <span class="text-body fw-normal"
                              >replied to your</span
                            >
                            <span class="text-primary fw-semibold">
                              Comment</span
                            >
                          </h6>
                          <small class="text-body fw-500">1 month ago</small>
                        </div>
                      </div>
                    </a>
                    <a href="#">
                      <div class="d-flex gap-3 mb-4">
                        <img
                          class="avatar-32 rounded-pill"
                          src="@/assets/images/user/03.jpg"
                          alt=""
                          loading="lazy"
                        />
                        <div>
                          <h6 class="font-size-14">
                            Esther Howard
                            <span class="text-body fw-normal"
                              >reacted comment in to your
                            </span>
                            <span class="text-primary fw-semibold">post</span>.
                          </h6>
                          <small class="text-body fw-500">19 min ago</small>
                        </div>
                      </div>
                    </a>
                  </div>
                  <button type="button" class="btn btn-primary fw-500 w-100">
                    View All Notifications
                  </button>
                </div>
              </div>
            </div>
          </li>

          <li class="nav-item dropdown user-dropdown">
            <a
              href="#"
              class="d-flex align-items-center dropdown-toggle"
              id="drop-down-arrow"
              data-bs-toggle="dropdown"
              aria-haspopup="true"
              aria-expanded="false"
            >
              <img
                src="@/assets/images/user/1.jpg"
                class="img-fluid rounded-circle avatar-48 border border-2 me-3"
                alt="user"
                loading="lazy"
              />
              <div class="caption d-none d-lg-block">
                <!-- <h6 class="mb-0 line-height">Bni Cyst</h6> -->
              </div>
            </a>
            <div
              class="sub-drop dropdown-menu caption-menu"
              aria-labelledby="drop-down-arrow"
            >
              <div class="card shadow-none m-0">
                <div class="card-header">
                  <div class="header-title">
                    <h5 class="mb-0">Hello Bni Cyst</h5>
                  </div>
                </div>
                <div class="card-body p-0">
                  <div class="d-flex align-items-center iq-sub-card border-0">
                    <span class="material-symbols-outlined"> line_style </span>
                    <div class="ms-3">
                      <router-link
                        :to="{ name: 'social.profilemain' }"
                        class="mb-0 h6"
                      >
                        My Profile
                      </router-link>
                    </div>
                  </div>
                  <div class="d-flex align-items-center iq-sub-card border-0">
                    <span class="material-symbols-outlined"> edit_note </span>
                    <div class="ms-3">
                      <router-link
                        :to="{ name: 'user.profile-edit' }"
                        class="mb-0 h6"
                      >
                        Edit Profile
                      </router-link>
                    </div>
                  </div>
                  <div class="d-flex align-items-center iq-sub-card border-0">
                    <span class="material-symbols-outlined">
                      manage_accounts
                    </span>
                    <div class="ms-3">
                      <router-link
                        :to="{ name: 'user.accountsetting' }"
                        class="mb-0 h6"
                      >
                        Account settings
                      </router-link>
                    </div>
                  </div>
                  <div class="d-flex align-items-center iq-sub-card border-0">
                    <span class="material-symbols-outlined"> lock </span>
                    <div class="ms-3">
                      <router-link
                        :to="{ name: 'user.privacy-setting' }"
                        class="mb-0 h6"
                      >
                        Privacy Settings
                      </router-link>
                    </div>
                  </div>
                  <div class="d-flex align-items-center iq-sub-card">
                    <span class="material-symbols-outlined"> login </span>
                    <div class="ms-3">
                      <router-link
                        :to="{ name: 'auth1.sign-in1' }"
                        class="mb-0 h6"
                      >
                        Sign out
                      </router-link>
                    </div>
                  </div>
                  <div class="iq-sub-card">
                    <h5>Chat Settings</h5>
                  </div>
                  <div class="d-flex align-items-center iq-sub-card border-0">
                    <i class="material-symbols-outlined text-success md-14">
                      circle
                    </i>
                    <div class="ms-3">Online</div>
                  </div>
                  <div class="d-flex align-items-center iq-sub-card border-0">
                    <i class="material-symbols-outlined text-warning md-14">
                      circle
                    </i>
                    <div class="ms-3">Away</div>
                  </div>
                  <div class="d-flex align-items-center iq-sub-card border-0">
                    <i class="material-symbols-outlined text-danger md-14">
                      circle
                    </i>
                    <div class="ms-3">Disconnected</div>
                  </div>
                  <div class="d-flex align-items-center iq-sub-card border-0">
                    <i class="material-symbols-outlined text-gray md-14">
                      circle
                    </i>
                    <div class="ms-3">Invisible</div>
                  </div>
                </div>
              </div>
            </div>
          </li>
        </ul>
      </div>
    </nav>
  </div>
</template>
<script>
import { useSetting } from "../../../../store/pinia";
import { computed } from "vue";
export default {
  name: "DefaultHeader",
  props: {
    image: {
      type: String,
      default: require("@/assets/images/logo.png"),
    },
  },
  setup() {
    const store = useSetting();
    const sidebarType = computed(() => store.sidebar_type_value);
    const appName = computed(() => store.app_name_value);

    const toggleSidebar = () => {
      document
        .getElementsByTagName("ASIDE")[0]
        .classList.toggle("sidebar-mini");
    };
    const toggleSearchModal = () => {
    const searchModal = document.querySelector('#search-modal');
    document.querySelector('#exampleModalFullscreenSm').addEventListener('shown.bs.modal', function () {
        const modalbackdrop = document.querySelector('.modal-backdrop')
        modalbackdrop.style.display = 'none';
    })
     if(searchModal.classList.contains('open')){
      searchModal.classList.remove('open')
     }
     else{
      searchModal.classList.add('open')
     }
  };
    return {
      store,
      sidebarType,
      toggleSidebar,
      toggleSearchModal,
      appName,
    };
  },
  methods: {
    checkActive(route) {
      if (this.$route.name === route) {
        return true;
      }
      if (route.includes(this.$route.name)) {
        return true;
      }
    },
  },
};
</script>
