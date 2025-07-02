<template>
  <div class="content-inner">
    <b-container>
      <b-row>
        <b-col sm="12" v-for="(item, index) in friendRequest" :key="index">
          <iq-card :body-class="item.bodyClass">
            <template v-slot:headerTitle>
              <h4 class="card-title">{{ item.title }}</h4>
            </template>
            <template v-slot:body>
              <ul class="request-list list-inline m-0 p-0">
                <li
                  :class="`d-flex align-items-center justify-content-between flex-wrap ${list.border}`"
                  v-for="(list, index1) in item.list"
                  :key="index1"
                >
                  <div class="user-img img-fluid flex-shrink-0">
                    <img
                      :src="list.img"
                      alt="story-img"
                      class="rounded-circle avatar-40"
                    />
                  </div>
                  <div class="flex-grow-1 ms-3">
                    <h6>{{ list.name }}</h6>
                    <p class="mb-0">{{ list.friend }}</p>
                  </div>
                  <div class="d-flex align-items-center mt-2 mt-md-0">
                    <div
                      :class="
                        list.confirmClickBtn === true ? 'confirm-click-btn' : ''
                      "
                    >
                      <a
                        href="#"
                        :class="`me-2 btn btn-${list.btncolor}-subtle rounded confirm-btn p-1 lh-1`"
                      >
                        <i class="material-symbols-outlined font-size-14">
                          {{ list.icon }}
                        </i>
                      </a>
                      <a
                        href="@/app/profile.html"
                        class="me-3 btn btn-primary rounded request-btn"
                        style="display: none"
                      ></a>
                    </div>
                    <a
                      href="#"
                      class="btn btn-danger-subtle rounded p-1 lh-1"
                      data-extra-toggle="delete"
                      data-closest-elem=".item"
                      @click="deleterequest"
                      ><i class="material-symbols-outlined font-size-14">
                        close
                      </i></a
                    >
                  </div>
                </li>
                <li
                  class="d-block text-center mb-0 pb-0"
                  v-if="item.title == 'Friend Request'"
                >
                  <a href="#" class="me-3 btn btn-primary">View More Request</a>
                </li>
              </ul>
            </template>
          </iq-card>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>
<script>
import { socialvue } from "../../../config/pluginInit";
export default {
  name: "FriendRequest",
  mounted() {
    socialvue.index();
  },
  data() {
    return {
      friendRequest: [
        {
          title: "Friend Request",
          bodyClass: "pt-0",
          btn1: "Confirm",
          btn2: "Delete Request",
          list: [
            {
              img: require("../../../assets/images/user/05.jpg"),
              name: "Jaques Amole",
              friend: "40  friends",
              icon: "done",
              btncolor: "success",
              border: "",
              confirmClickBtn: true,
            },
            {
              img: require("../../../assets/images/user/06.jpg"),
              name: "Lucy Tania",
              friend: "12  friends",
              icon: "done",
              btncolor: "success",
              border: "",
              confirmClickBtn: true,
            },
            {
              img: require("../../../assets/images/user/07.jpg"),
              name: "Val Adictorian",
              friend: "0  friends",
              icon: "done",
              btncolor: "success",
              border: "",
              confirmClickBtn: true,
            },
            {
              img: require("../../../assets/images/user/08.jpg"),
              name: "Manny Petty",
              friend: "3  friends",
              icon: "done",
              btncolor: "success",
              border: "",
              confirmClickBtn: false,
            },
            {
              img: require("../../../assets/images/user/09.jpg"),
              name: "Marsha Mello",
              friend: "15  friends",
              icon: "done",
              btncolor: "success",
              border: "",
              confirmClickBtn: false,
            },
            {
              img: require("../../../assets/images/user/10.jpg"),
              name: "Caire Innet",
              friend: "8  friends",
              icon: "done",
              btncolor: "success",
              border: "",
              confirmClickBtn: false,
            },
            {
              img: require("../../../assets/images/user/11.jpg"),
              name: "Gio Metric",
              friend: "10  friends",
              icon: "done",
              btncolor: "success",
              border: "",
              confirmClickBtn: false,
            },
            {
              img: require("../../../assets/images/user/12.jpg"),
              name: "Chris P. Cream",
              friend: "18  friends",
              icon: "done",
              btncolor: "success",
              border: "",
              confirmClickBtn: false,
            },
            {
              img: require("../../../assets/images/user/13.jpg"),
              name: "Paul Misunday",
              friend: "6  friends",
              icon: "done",
              btncolor: "success",
              border: "",
              confirmClickBtn: false,
            },
            {
              img: require("../../../assets/images/user/14.jpg"),
              name: "Reanne Carnation",
              friend: "12  friends",
              icon: "done",
              btncolor: "success",
              border: "border-0",
              confirmClickBtn: false,
            },
          ],
        },
        {
          title: "People You May Know",
          list: [
            {
              img: require("../../../assets/images/user/15.jpg"),
              name: "Jen Youfelct",
              friend: "4 friends",
              icon: "add",
              btncolor: "primary",
              border: "",
            },
            {
              img: require("../../../assets/images/user/16.jpg"),
              name: "Cooke Edoh",
              friend: "30  friends",
              icon: "add",
              btncolor: "primary",
              border: "",
            },
            {
              img: require("../../../assets/images/user/17.jpg"),
              name: "Earl E. Riser",
              friend: "30  friends",
              icon: "add",
              btncolor: "primary",
              border: "",
            },
            {
              img: require("../../../assets/images/user/05.jpg"),
              name: "Cliff Diver",
              friend: "5  friends",
              icon: "add",
              btncolor: "primary",
              border: "",
            },
            {
              img: require("../../../assets/images/user/06.jpg"),
              name: "Cliff Diver",
              friend: "5  friends",
              icon: "add",
              btncolor: "primary",
              border: "",
            },
            {
              img: require("../../../assets/images/user/07.jpg"),
              name: "Vinny Gret",
              friend: "50  friends",
              icon: "add",
              btncolor: "primary",
              border: "",
            },
            {
              img: require("../../../assets/images/user/08.jpg"),
              name: "Paul Samic",
              friend: "6  friends",
              icon: "add",
              btncolor: "primary",
              border: "",
            },
            {
              img: require("../../../assets/images/user/09.jpg"),
              name: "Gustav Wind",
              friend: "14  friends",
              icon: "add",
              btncolor: "primary",
              border: "",
            },
            {
              img: require("../../../assets/images/user/10.jpg"),
              name: "Minnie Strone",
              friend: "16  friends",
              icon: "add",
              btncolor: "primary",
              border: "",
            },
            {
              img: require("../../../assets/images/user/11.jpg"),
              name: "Ray Volver",
              friend: "9  friends",
              icon: "add",
              btncolor: "primary",
              border: "",
            },
            {
              img: require("../../../assets/images/user/12.jpg"),
              name: "Indy Nile",
              friend: "6  friends",
              icon: "add",
              btncolor: "primary",
              border: "",
            },
            {
              img: require("../../../assets/images/user/13.jpg"),
              name: "Jen Trification",
              friend: "42  friends",
              icon: "add",
              btncolor: "primary",
              border: "border-0",
            },
          ],
        },
      ],
    };
  },
  methods: {
    deleterequest() {
      const swalWithBootstrapButtons = this.$swal.mixin({
        customClass: {
          confirmButton: "btn btn-primary btn-lg",
          cancelButton: "btn btn-outline-primary btn-lg ms-2",
        },
        buttonsStyling: false,
      });

      swalWithBootstrapButtons
        .fire({
          title: "Are you sure?",
          text: "You won't be able to revert this!",
          icon: "warning",
          showCancelButton: true,
          confirmButtonText: "Yes, delete it!",
          showClass: {
            popup: "animate__animated animate__zoomIn",
          },
          hideClass: {
            popup: "animate__animated animate__zoomOut",
          },
        })
        .then((willDelete) => {
          if (willDelete.isConfirmed) {
            swalWithBootstrapButtons.fire({
              title: "Deleted!",
              text: "Your Request has been deleted.",
              icon: "success",
              showClass: {
                popup: "animate__animated animate__zoomIn",
              },
              hideClass: {
                popup: "animate__animated animate__zoomOut",
              },
            });
          } else {
            swalWithBootstrapButtons.fire({
              title: "Your Request is safe!",
              showClass: {
                popup: "animate__animated animate__zoomIn",
              },
              hideClass: {
                popup: "animate__animated animate__zoomOut",
              },
            });
          }
        });
    },
  },
};
</script>
