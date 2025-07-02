<template>
  <div class="friend-list-tab mt-2">
    <tab-nav
      :pills="true"
      id="tab"
      class="nav nav-pills d-flex align-items-center justify-content-left list-item-tabs p-0 mb-2"
    >
      <tab-nav-items active
        :liClass="{ active: activeTab === 'all-friends' }"
        id="pills-all-friends"
        href="#all-friends"
        ariaControls="pills-all-friends"
        role="tab"
        :ariaSelected="activeTab === 'all-friends'"
        title="All Friends"
        @click="activeTab = 'all-friends'"
      />
      <tab-nav-items
        :liClass="{ active: activeTab === 'recently-add' }"
        id="pills-recently-add"
        href="#recently-add"
        ariaControls="pills-recently-add"
        role="tab"
        :ariaSelected="activeTab === 'recently-add'"
        title="Recently Added"
        @click="activeTab = 'recently-add'"
      />
      <tab-nav-items
        :liClass="{ active: activeTab === 'closefriends' }"
        id="pills-closefriends"
        href="#closefriends"
        ariaControls="pills-closefriends"
        role="tab"
        :ariaSelected="activeTab === 'closefriends'"
        title="Close friends"
        @click="activeTab = 'closefriends'"
      />
      <tab-nav-items
        :liClass="{ active: activeTab === 'home' }"
        id="pills-home"
        href="#home"
        ariaControls="pills-home"
        role="tab"
        :ariaSelected="activeTab === 'home'"
        title="Home/Town"
        @click="activeTab = 'home'"
      />
      <tab-nav-items
        :liClass="{ active: activeTab === 'following-add' }"
        id="pills-following-add"
        href="#following-add"
        ariaControls="pills-following-add"
        role="tab"
        :ariaSelected="activeTab === 'following-add'"
        title="Following"
        @click="activeTab = 'following-add'"
      />
    </tab-nav>
    <div class="tab-content">
      <tab-content-item
        :active="activeTab === 'all-friends'"
        id="all-friends"
        aria-labelled-by="pills-all-friends"
      >
        <div class="iq-card-body p-0">
          <div class="row">
            <div
              class="col-md-6 col-lg-6 mb-3"
              v-for="(friend, index) in friends"
              :key="index"
            >
              <div class="iq-friendlist-block">
                <div class="d-flex align-items-center justify-content-between">
                  <div class="d-flex align-items-center">
                    <a href="#">
                      <img
                        :src="friend.img"
                        alt="profile-img"
                        class="img-fluid"
                      />
                    </a>
                    <div class="friend-info ms-3">
                      <h5>{{ friend.name }}</h5>
                      <p class="mb-0">{{ friend.friend }}</p>
                    </div>
                  </div>
                  <div class="iq-card-header-toolbar d-flex align-items-center">
                    <div class="dropdown">
                      <span
                        class="dropdown btn btn-secondary me-2 d-flex align-items-center"
                        id="dropdownMenuButton01"
                        data-bs-toggle="dropdown"
                        aria-expanded="true"
                        role="button"
                      >
                        <i class="material-symbols-outlined me-2"> done </i>
                        Friend
                      </span>
                      <div
                        class="dropdown-menu dropdown-menu-right"
                        aria-labelledby="dropdownMenuButton01"
                      >
                        <a class="dropdown-item" href="#">Get Notification</a>
                        <a class="dropdown-item" href="#">Close Friend</a>
                        <a class="dropdown-item" href="#">Unfollow</a>
                        <a class="dropdown-item" href="#">Unfriend</a>
                        <a class="dropdown-item" href="#">Block</a>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </tab-content-item>
    </div>
    <div class="tab-content">
      <tab-content-item
        :active="activeTab === 'recently-add'"
        id="recently-add"
        aria-labelled-by="pills-recently-add"
      >
        <div class="iq-card-body p-0">
          <div class="row">
            <div
              class="col-md-6 col-lg-6 mb-3"
              v-for="(items, index) in recentlyadded"
              :key="index"
            >
              <div class="iq-friendlist-block">
                <div class="d-flex align-items-center justify-content-between">
                  <div class="d-flex align-items-center">
                    <a href="#">
                      <img
                        :src="items.img"
                        alt="profile-img"
                        class="img-fluid"
                      />
                    </a>
                    <div class="friend-info ms-3">
                      <h5>{{ items.name }}</h5>
                      <p class="mb-0">{{ items.friend }}</p>
                    </div>
                  </div>
                  <div class="iq-card-header-toolbar d-flex align-items-center">
                    <div class="dropdown">
                      <span
                        class="dropdown btn btn-secondary me-2 d-flex align-items-center"
                        id="dropdownMenuButton01"
                        data-bs-toggle="dropdown"
                        aria-expanded="true"
                        role="button"
                      >
                        <i class="material-symbols-outlined me-2"> done </i>
                        Friend
                      </span>
                      <div
                        class="dropdown-menu dropdown-menu-right"
                        aria-labelledby="dropdownMenuButton01"
                      >
                        <a class="dropdown-item" href="#">Get Notification</a>
                        <a class="dropdown-item" href="#">Close Friend</a>
                        <a class="dropdown-item" href="#">Unfollow</a>
                        <a class="dropdown-item" href="#">Unfriend</a>
                        <a class="dropdown-item" href="#">Block</a>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </tab-content-item>
    </div>
    <div class="tab-content">
      <tab-content-item
        :active="activeTab === 'closefriends'"
        id="closefriends"
        aria-labelled-by="pills-closefriends"
      >
        <div class="iq-card-body p-0">
          <div class="row">
            <div
              class="col-md-6 col-lg-6 mb-3"
              v-for="(items, index) in closeFriend"
              :key="index"
            >
              <div class="iq-friendlist-block">
                <div class="d-flex align-items-center justify-content-between">
                  <div class="d-flex align-items-center">
                    <a href="#">
                      <img
                        :src="items.img"
                        alt="profile-img"
                        class="img-fluid"
                      />
                    </a>
                    <div class="friend-info ms-3">
                      <h5>{{ items.name }}</h5>
                      <p class="mb-0">{{ items.friend }}</p>
                    </div>
                  </div>
                  <div class="iq-card-header-toolbar d-flex align-items-center">
                    <div class="dropdown">
                      <span
                        class="dropdown btn btn-secondary me-2 d-flex align-items-center"
                        id="dropdownMenuButton01"
                        data-bs-toggle="dropdown"
                        aria-expanded="true"
                        role="button"
                      >
                        <i class="material-symbols-outlined me-2"> done </i>
                        Friend
                      </span>
                      <div
                        class="dropdown-menu dropdown-menu-right"
                        aria-labelledby="dropdownMenuButton01"
                      >
                        <a class="dropdown-item" href="#">Get Notification</a>
                        <a class="dropdown-item" href="#">Close Friend</a>
                        <a class="dropdown-item" href="#">Unfollow</a>
                        <a class="dropdown-item" href="#">Unfriend</a>
                        <a class="dropdown-item" href="#">Block</a>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </tab-content-item>
    </div>
    <div class="tab-content">
      <tab-content-item
        :active="activeTab === 'home'"
        id="home"
        aria-labelled-by="pills-home"
      >
        <div class="iq-card-body p-0">
          <div class="row">
            <div
              class="col-md-6 col-lg-6 mb-3"
              v-for="(items, index) in homeTown"
              :key="index"
            >
              <div class="iq-friendlist-block">
                <div class="d-flex align-items-center justify-content-between">
                  <div class="d-flex align-items-center">
                    <a href="#">
                      <img
                        :src="items.img"
                        alt="profile-img"
                        class="img-fluid"
                      />
                    </a>
                    <div class="friend-info ms-3">
                      <h5>{{ items.name }}</h5>
                      <p class="mb-0">{{ items.friend }}</p>
                    </div>
                  </div>
                  <div class="iq-card-header-toolbar d-flex align-items-center">
                    <div class="dropdown">
                      <span
                        class="dropdown btn btn-secondary me-2 d-flex align-items-center"
                        id="dropdownMenuButton01"
                        data-bs-toggle="dropdown"
                        aria-expanded="true"
                        role="button"
                      >
                        <i class="material-symbols-outlined me-2"> done </i>
                        Friend
                      </span>
                      <div
                        class="dropdown-menu dropdown-menu-right"
                        aria-labelledby="dropdownMenuButton01"
                      >
                        <a class="dropdown-item" href="#">Get Notification</a>
                        <a class="dropdown-item" href="#">Close Friend</a>
                        <a class="dropdown-item" href="#">Unfollow</a>
                        <a class="dropdown-item" href="#">Unfriend</a>
                        <a class="dropdown-item" href="#">Block</a>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </tab-content-item>
    </div>
    <div class="tab-content">
      <tab-content-item
        :active="activeTab === 'following-add'"
        id="following-add"
        aria-labelled-by="pills-following-add"
      >
        <div class="iq-card-body p-0">
          <div class="row">
            <div
              class="col-md-6 col-lg-6 mb-3"
              v-for="(items, index) in following"
              :key="index"
            >
              <div class="iq-friendlist-block">
                <div class="d-flex align-items-center justify-content-between">
                  <div class="d-flex align-items-center">
                    <a href="#">
                      <img
                        :src="items.img"
                        alt="profile-img"
                        class="img-fluid"
                      />
                    </a>
                    <div class="friend-info ms-3">
                      <h5>{{ items.name }}</h5>
                      <p class="mb-0">{{ items.friend }}</p>
                    </div>
                  </div>
                  <div class="iq-card-header-toolbar d-flex align-items-center">
                    <div class="dropdown">
                      <span
                        class="dropdown btn btn-secondary me-2 d-flex align-items-center"
                        id="dropdownMenuButton01"
                        data-bs-toggle="dropdown"
                        aria-expanded="true"
                        role="button"
                      >
                        <i class="material-symbols-outlined me-2"> done </i>
                        Friend
                      </span>
                      <div
                        class="dropdown-menu dropdown-menu-right"
                        aria-labelledby="dropdownMenuButton01"
                      >
                        <a class="dropdown-item" href="#">Get Notification</a>
                        <a class="dropdown-item" href="#">Close Friend</a>
                        <a class="dropdown-item" href="#">Unfollow</a>
                        <a class="dropdown-item" href="#">Unfriend</a>
                        <a class="dropdown-item" href="#">Block</a>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </tab-content-item>
    </div>
  </div>
</template>
<script>
export default {
  name: "FriendTab",
  data() {
    return {
      activeTab: "all-friends",
      friends: [
        {
          img: require("../../../../assets/images/user/05.jpg"),
          name: "Petey Cruiser",
          friend: "15 friends",
        },
        {
          img: require("../../../../assets/images/user/06.jpg"),
          name: "Anna Sthesia",
          friend: "50  friends",
        },
        {
          img: require("../../../../assets/images/user/07.jpg"),
          name: "Paul Molive",
          friend: "10  friends",
        },
        {
          img: require("../../../../assets/images/user/08.jpg"),
          name: "Gail Forcewind",
          friend: "20 friends",
        },
        {
          img: require("../../../../assets/images/user/09.jpg"),
          name: "Paige Turner",
          friend: "12  friends",
        },
        {
          img: require("../../../../assets/images/user/10.jpg"),
          name: "B Frapples",
          friend: "6  friends",
        },
        {
          img: require("../../../../assets/images/user/13.jpg"),
          name: "Walter Melon",
          friend: "30  friends",
        },
        {
          img: require("../../../../assets/images/user/14.jpg"),
          name: "Barb Ackue",
          friend: "14  friends",
        },
        {
          img: require("../../../../assets/images/user/15.jpg"),
          name: "Buck Kinnear",
          friend: "16 friends",
        },
        {
          img: require("../../../../assets/images/user/16.jpg"),
          name: "Ira Membrit",
          friend: "22 friends",
        },
        {
          img: require("../../../../assets/images/user/17.jpg"),
          name: "Shonda Leer",
          friend: "10 friends",
        },
        {
          img: require("../../../../assets/images/user/18.jpg"),
          name: "Ock Lee",
          friend: "18 friends",
        },
        {
          img: require("../../../../assets/images/user/19.jpg"),
          name: "Maya Didas",
          friend: "40 friends",
        },
        {
          img: require("../../../../assets/images/user/05.jpg"),
          name: "Rick OShea",
          friend: "50 friends",
        },
        {
          img: require("../../../../assets/images/user/06.jpg"),
          name: "Pete Sariya",
          friend: "5 friends",
        },
        {
          img: require("../../../../assets/images/user/07.jpg"),
          name: "Monty Carlo",
          friend: "2 friends",
        },
        {
          img: require("../../../../assets/images/user/08.jpg"),
          name: "Sal Monella",
          friend: "0 friends",
        },
        {
          img: require("../../../../assets/images/user/09.jpg"),
          name: "Sue Vaneer",
          friend: "25 friends",
        },
        {
          img: require("../../../../assets/images/user/10.jpg"),
          name: "Cliff Hanger",
          friend: "18 friends",
        },
        {
          img: require("../../../../assets/images/user/05.jpg"),
          name: "Barb Dwyer",
          friend: "23 friends",
        },
        {
          img: require("../../../../assets/images/user/06.jpg"),
          name: "Terry Aki",
          friend: "8 friends",
        },
        {
          img: require("../../../../assets/images/user/13.jpg"),
          name: "Cory Ander",
          friend: "7 friends",
        },
        {
          img: require("../../../../assets/images/user/14.jpg"),
          name: "Robin Banks",
          friend: "14 friends",
        },
        {
          img: require("../../../../assets/images/user/15.jpg"),
          name: "Jimmy Changa",
          friend: "10 friends",
        },
        {
          img: require("../../../../assets/images/user/16.jpg"),
          name: "Barry Wine",
          friend: "18 friends",
        },
        {
          img: require("../../../../assets/images/user/17.jpg"),
          name: "Poppa Cherry",
          friend: "16 friends",
        },
        {
          img: require("../../../../assets/images/user/18.jpg"),
          name: "Zack Lee",
          friend: "33 friends",
        },
        {
          img: require("../../../../assets/images/user/19.jpg"),
          name: "Don Stairs",
          friend: "15 friends",
        },
        {
          img: require("../../../../assets/images/user/05.jpg"),
          name: "Peter Pants",
          friend: "12 friends",
        },
        {
          img: require("../../../../assets/images/user/06.jpg"),
          name: "Hal Appeno",
          friend: "13 friends",
        },
      ],
      recentlyadded: [
        {
          img: require("../../../../assets/images/user/15.jpg"),
          name: "Polly Tech",
          friend: "10 friends",
        },
        {
          img: require("../../../../assets/images/user/16.jpg"),
          name: "Holly Graham",
          friend: "8  friends",
        },
        {
          img: require("../../../../assets/images/user/17.jpg"),
          name: "Tara Zona",
          friend: "5  friends",
        },
        {
          img: require("../../../../assets/images/user/18.jpg"),
          name: "Barry Cade",
          friend: "20  friends",
        },
      ],
      closeFriend: [
        {
          img: require("../../../../assets/images/user/19.jpg"),
          name: "Bud Wiser",
          friend: "32  friends",
        },
        {
          img: require("../../../../assets/images/user/05.jpg"),
          name: "Otto Matic",
          friend: "9  friends",
        },
        {
          img: require("../../../../assets/images/user/06.jpg"),
          name: "Peter Pants",
          friend: "2  friends",
        },
        {
          img: require("../../../../assets/images/user/07.jpg"),
          name: "Zack Lee",
          friend: "15  friends",
        },
        {
          img: require("../../../../assets/images/user/08.jpg"),
          name: "Barry Wine",
          friend: "36  friends",
        },
        {
          img: require("../../../../assets/images/user/09.jpg"),
          name: "Robin Banks",
          friend: "22  friends",
        },
        {
          img: require("../../../../assets/images/user/10.jpg"),
          name: "Cory Ander",
          friend: "18  friends",
        },
        {
          img: require("../../../../assets/images/user/15.jpg"),
          name: "Moe Fugga",
          friend: "12  friends",
        },
        {
          img: require("../../../../assets/images/user/16.jpg"),
          name: "Polly Tech",
          friend: "30   friends",
        },
        {
          img: require("../../../../assets/images/user/17.jpg"),
          name: "Hal Appeno",
          friend: "25  friends",
        },
      ],
      homeTown: [
        {
          img: require("../../../../assets/images/user/18.jpg"),
          name: "Paul Molive",
          friend: "14  friends",
        },
        {
          img: require("../../../../assets/images/user/19.jpg"),
          name: "Paige Turner",
          friend: "8  friends",
        },
        {
          img: require("../../../../assets/images/user/05.jpg"),
          name: "Barb Ackue",
          friend: "23  friends",
        },
        {
          img: require("../../../../assets/images/user/06.jpg"),
          name: "Ira Membrit",
          friend: "16  friends",
        },
        {
          img: require("../../../../assets/images/user/07.jpg"),
          name: "Maya Didas",
          friend: "12  friends",
        },
      ],
      following: [
        {
          img: require("../../../../assets/images/user/05.jpg"),
          name: "Maya Didas",
          friend: "15  friends",
        },
        {
          img: require("../../../../assets/images/user/16.jpg"),
          name: "Monty Carlo",
          friend: "3  friends",
        },
        {
          img: require("../../../../assets/images/user/07.jpg"),
          name: "Cliff Hanger",
          friend: "20  friends",
        },
        {
          img: require("../../../../assets/images/user/08.jpg"),
          name: "B Ackue",
          friend: "12  friends",
        },
        {
          img: require("../../../../assets/images/user/09.jpg"),
          name: "Bob Frapples",
          friend: "12  friends",
        },
        {
          img: require("../../../../assets/images/user/10.jpg"),
          name: "Anna Mull",
          friend: "06  friends",
        },
        {
          img: require("../../../../assets/images/user/15.jpg"),
          name: "Ry Wine",
          friend: "15  friends",
        },
        {
          img: require("../../../../assets/images/user/16.jpg"),
          name: "Don Stairs",
          friend: "12  friends",
        },
        {
          img: require("../../../../assets/images/user/17.jpg"),
          name: "Peter Pants",
          friend: "08  friends",
        },
        {
          img: require("../../../../assets/images/user/18.jpg"),
          name: "Polly Tech",
          friend: "18  friends",
        },
        {
          img: require("../../../../assets/images/user/19.jpg"),
          name: "Tara Zona",
          friend: "30  friends",
        },
        {
          img: require("../../../../assets/images/user/05.jpg"),
          name: "Arty Ficial",
          friend: "15  friends",
        },
        {
          img: require("../../../../assets/images/user/06.jpg"),
          name: "Bill Emia",
          friend: "25  friends",
        },
        {
          img: require("../../../../assets/images/user/07.jpg"),
          name: "Bill Yerds",
          friend: "9  friends",
        },
        {
          img: require("../../../../assets/images/user/08.jpg"),
          name: "Matt Innae",
          friend: "19  friends",
        },
      ],
    };
  },
};
</script>
