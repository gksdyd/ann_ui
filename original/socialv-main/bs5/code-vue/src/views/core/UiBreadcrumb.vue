<template>
  <div class="content-inner">
    <b-container>
      <b-row>
        <b-col sm="12">
          <b-card
            no-body
            class="position-relative inner-page-bg bg-primary"
            style="height: 150px"
          >
            <div class="inner-page-title">
              <h3 class="text-white">Breadcrumb Page</h3>
              <p class="text-white">lorem ipsum</p>
            </div>
          </b-card>
        </b-col>
        <b-col lg="6" sm="12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Breadcrumb</h4>
            </template>
            <template v-slot:body>
              <p>
                Use the items in order to programatically generate the
                breadcrumb links.use class <code>.breadcrumb to ol</code>
              </p>
              <nav aria-label="breadcrumb ">
                <ol class="breadcrumb bg-primary-subtle">
                  <li class="breadcrumb-item active" aria-current="page">
                    Home
                  </li>
                </ol>
              </nav>
              <nav aria-label="breadcrumb">
                <ol class="breadcrumb bg-primary-subtle">
                  <li class="breadcrumb-item"><a href="#">Home</a></li>
                  <li class="breadcrumb-item active" aria-current="page">
                    Library
                  </li>
                </ol>
              </nav>
              <nav aria-label="breadcrumb">
                <ol class="breadcrumb bg-primary-subtle">
                  <li class="breadcrumb-item"><a href="#">Home</a></li>
                  <li class="breadcrumb-item"><a href="#">Library</a></li>
                  <li class="breadcrumb-item active" aria-current="page">
                    Data
                  </li>
                </ol>
              </nav>
            </template>
          </iq-card>
        </b-col>
        <b-col lg="6" sm="12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Breadcrumb With Icon</h4>
            </template>
            <template v-slot:body>
              <p>
                Use the items in order to programatically generate the
                breadcrumb links.use class <code>.breadcrumb to ol</code> with
                Icon
              </p>
              <nav aria-label="breadcrumb ">
                <ol class="breadcrumb bg-primary-subtle">
                  <li class="breadcrumb-item active d-flex" aria-current="page">
                    <i class="material-symbols-outlined me-1">home</i>Home
                  </li>
                </ol>
              </nav>
              <nav aria-label="breadcrumb ">
                <ol class="breadcrumb bg-primary-subtle">
                  <li class="breadcrumb-item d-flex" aria-current="page">
                    <a href="#">
                      <i class="material-symbols-outlined me-1">home</i>
                    </a>
                  </li>
                  <li class="breadcrumb-item active" aria-current="page">
                    Library
                  </li>
                </ol>
              </nav>
              <nav aria-label="breadcrumb">
                <ol class="breadcrumb bg-primary-subtle">
                  <li class="breadcrumb-item">
                    <a href="#"
                      ><i class="material-symbols-outlined me-1">home</i></a
                    >
                  </li>
                  <a href="#">Library</a>
                  <li class="breadcrumb-item"></li>
                  <li class="breadcrumb-item active" aria-current="page">
                    Data
                  </li>
                </ol>
              </nav>
            </template>
          </iq-card>
        </b-col>
      </b-row>
      <div class="row">
        <b-col lg="6" sm="12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Breadcrumb</h4>
            </template>
            <template v-slot:body>
              <p>use class <code>.breadcrumb .bg-primary</code></p>
              <nav aria-label="breadcrumb ">
                <ol class="breadcrumb bg-primary">
                  <li
                    class="breadcrumb-item active text-white"
                    aria-current="page"
                  >
                    Home
                  </li>
                </ol>
              </nav>
              <nav aria-label="breadcrumb">
                <ol class="breadcrumb bg-primary">
                  <li class="breadcrumb-item">
                    <a href="#" class="text-white">Home</a>
                  </li>
                  <li
                    class="breadcrumb-item active text-white"
                    aria-current="page"
                  >
                    Library
                  </li>
                </ol>
              </nav>
              <nav aria-label="breadcrumb">
                <ol class="breadcrumb bg-primary mb-0">
                  <li class="breadcrumb-item">
                    <a href="#" class="text-white">Home</a>
                  </li>
                  <li class="breadcrumb-item">
                    <a href="#" class="text-white">Library</a>
                  </li>
                  <li
                    class="breadcrumb-item active text-white"
                    aria-current="page"
                  >
                    Data
                  </li>
                </ol>
              </nav>
            </template>
          </iq-card>
        </b-col>
        <b-col lg="6" sm="12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Breadcrumb With Icon</h4>
            </template>
            <template v-slot:body>
              <p>use class <code>.breadcrumb .bg-primary </code> With Icon.</p>
              <nav aria-label="breadcrumb">
                <ol class="breadcrumb bg-primary">
                  <li
                    class="d-flex breadcrumb-item active text-white"
                    aria-current="page"
                  >
                    <i class="material-symbols-outlined me-1">home</i>Home
                  </li>
                </ol>
              </nav>
              <nav aria-label="breadcrumb">
                <ol class="breadcrumb bg-primary">
                  <li class="breadcrumb-item">
                    <a href="#" class="text-white"
                      ><i class="material-symbols-outlined me-1">home</i></a
                    >
                  </li>
                  <li
                    class="breadcrumb-item active text-white"
                    aria-current="page"
                  >
                    Library
                  </li>
                </ol>
              </nav>
              <nav aria-label="breadcrumb">
                <ol class="breadcrumb bg-primary mb-0">
                  <li class="breadcrumb-item">
                    <a href="#" class="text-white"
                      ><i class="material-symbols-outlined me-1">home</i></a
                    >
                  </li>
                  <a href="#" class="text-white">Library</a>
                  <li class="breadcrumb-item"></li>
                  <li
                    class="breadcrumb-item active text-white"
                    aria-current="page"
                  >
                    Data
                  </li>
                </ol>
              </nav>
            </template>
          </iq-card>
        </b-col>
        <b-col lg="6" sm="12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Breadcrumb With Icon</h4>
            </template>
            <template v-slot:body>
              <p>use class <code>.breadcrumb .iq-bg-primary</code></p>
              <nav aria-label="breadcrumb">
                <ol class="breadcrumb bg-primary-subtle">
                  <li class="d-flex breadcrumb-item active" aria-current="page">
                    <i class="material-symbols-outlined me-1">home</i>Home
                  </li>
                </ol>
              </nav>
              <nav aria-label="breadcrumb">
                <ol class="breadcrumb bg-primary-subtle">
                  <li class="breadcrumb-item">
                    <a href="#"
                      ><i class="material-symbols-outlined me-1">home</i></a
                    >
                  </li>
                  <li class="breadcrumb-item active" aria-current="page">
                    Library
                  </li>
                </ol>
              </nav>
              <nav aria-label="breadcrumb">
                <ol class="breadcrumb bg-primary-subtle">
                  <li class="breadcrumb-item">
                    <a href="#"
                      ><i class="material-symbols-outlined me-1">home</i></a
                    >
                  </li>
                  <a href="#">Library</a>
                  <li class="breadcrumb-item"></li>
                  <li class="breadcrumb-item active" aria-current="page">
                    Data
                  </li>
                </ol>
              </nav>
            </template>
          </iq-card>
        </b-col>
        <b-col lg="6" sm="12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Breadcrumb With Icon</h4>
            </template>
            <template v-slot:body>
              <p>use class <code>.breadcrumb .iq-bg-danger</code></p>
              <nav aria-label="breadcrumb bg-danger-subtle">
                <ol class="breadcrumb bg-danger-subtle">
                  <li class="d-flex breadcrumb-item active" aria-current="page">
                    <i class="material-symbols-outlined me-1">home</i>Home
                  </li>
                </ol>
              </nav>
              <nav aria-label="breadcrumb bg-danger-subtle">
                <ol class="breadcrumb bg-danger-subtle">
                  <li class="breadcrumb-item">
                    <a href="#" class="text-danger"
                      ><i class="material-symbols-outlined me-1">home</i></a
                    >
                  </li>
                  <li class="breadcrumb-item active" aria-current="page">
                    Library
                  </li>
                </ol>
              </nav>
              <nav aria-label="breadcrumb bg-danger-subtle">
                <ol class="breadcrumb bg-danger-subtle">
                  <li class="breadcrumb-item">
                    <a href="#" class="text-danger"
                      ><i class="material-symbols-outlined me-1">home</i></a
                    >
                  </li>
                  <a href="#" class="text-danger">Library</a>
                  <li class="breadcrumb-item"></li>
                  <li class="breadcrumb-item active" aria-current="page">
                    Data
                  </li>
                </ol>
              </nav>
            </template>
          </iq-card>
        </b-col>
      </div>
    </b-container>
  </div>
</template>
<script>
// import { socialvue } from '../../config/pluginInit'

export default {
  name: "UiBreadcrumb",
  mounted() {
    // socialvue.index()
  },
  data() {
    return {
      items1: [
        {
          text: "Home",
          active: true,
        },
      ],
      items2: [
        {
          text: "Home",
          href: "#",
        },
        {
          text: "Library",
          active: true,
        },
      ],
      items3: [
        {
          text: "Home",
          href: "#",
        },
        {
          text: "Library",
          href: "#",
        },
        {
          text: "Data",
          active: true,
        },
      ],
      itemsIcon1: [
        {
          html: '<i class="ri-home-4-line mr-1 float-left"></i>Home',
          active: true,
        },
      ],
      itemsIcon2: [
        {
          html: '<i class="ri-home-4-line mr-1 float-left"></i>Home',
          href: "#",
        },
        {
          text: "Library",
          active: true,
        },
      ],
      itemsIcon3: [
        {
          html: '<i class="ri-home-4-line mr-1 float-left"></i>Home',
          href: "#",
        },
        {
          text: "Library",
          href: "#",
        },
        {
          text: "Data",
          active: true,
        },
      ],
    };
  },
};
</script>
