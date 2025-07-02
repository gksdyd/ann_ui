<template>
  <div class="row">
    <div class="col-sm-12">
      <iq-card>
        <template v-slot:body>
          <div
            class="d-flex justify-content-between align-items-center flex-wrap"
          >
            <div class="todo-date d-flex me-3 align-items-center">
              <i
                :class="`material-symbols-outlined text-success me-2 md-18-${category.color} me-2`"
                >calendar_month</i
              >
              <span>{{ project.project_name }}</span>
            </div>
            <div
              class="todo-notification d-flex align-items-center mt-2 mt-md-0"
            >
              <div
                class="notification-icon position-relative d-flex align-items-center me-3"
              >
                <a href="#" class="material-symbols-outlined md-18"
                  >notifications</a
                >
                <span class="bg-danger text-white">5</span>
              </div>
              <button type="submit" class="btn btn-success-subtle">
                Add Task
              </button>
              <TaskForm :new-id="taskList.length" :category="categoryList" />
            </div>
          </div>
        </template>
      </iq-card>
    </div>
    <div class="col-md-8">
      <iq-card body-class="p-0" v-if="taskList.length > 0">
        <template v-slot:body>
          <ul class="todo-task-lists m-0 p-0">
            <template v-for="(item, index) in taskList">
              <li
                class="d-flex align-items-center p-3"
                v-if="
                  (category.isHidden || item.category_id === category.id) &&
                  item.project_id === project.id
                "
                :key="index"
                :class="item.task_status ? 'active-task' : ''"
              >
                <div class="user-img img-fluid">
                  <img
                    :src="checkUser(item.id, 'image')"
                    alt="story-img"
                    class="rounded-circle avatar-40"
                  />
                </div>
                <div
                  class="d-flex align-items-center justify-content-between w-100"
                >
                  <div class="ms-3">
                    <h6 :class="item.dinlineblock">
                      {{ item.task_title }}
                    </h6>
                    {{ "" }}
                    <span
                      class="badge bg-warning ms-0 ms-md-3 my-1 my-md-0 text-white"
                      v-if="item.status === 'Expiring'"
                      >{{ item.status }}</span
                    >
                    <span
                      class="badge bg-success ms-0 ms-md-3 my-1 my-md-0"
                      v-if="item.status === 'Ending'"
                      >{{ item.status }}</span
                    >
                    <span
                      class="badge bg-danger ms-0 ms-md-3 my-1 my-md-0"
                      v-if="item.status === 'Urgent'"
                      >{{ item.status }}</span
                    >
                    <p class="mb-0">by {{ checkUser(item.user_id, "name") }}</p>
                  </div>
                  <div class="card-header-toolbar d-flex align-items-center">
                    <div class="form-check">
                      <input
                        type="checkbox"
                        name="todo-check"
                        class="form-check-input"
                        :id="'check' + index"
                        :checked="item.task_status"
                      />
                      <label
                        class="form-check-label"
                        :for="'check' + index"
                      ></label>
                    </div>
                  </div>
                </div>
              </li>
            </template>
          </ul>
        </template>
      </iq-card>
      <template v-else>
        <div class="text-center">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            xmlns:xlink="http://www.w3.org/1999/xlink"
            width="138"
            height="138"
            class="hits-empty-state-image"
          >
            <defs>
              <linearGradient id="c" x1="50%" x2="50%" y1="100%" y2="0%">
                <stop offset="0%" stop-color="#F5F5FA" />
                <stop offset="100%" stop-color="#FFF" />
              </linearGradient>
              <path
                id="b"
                d="M68.71 114.25a45.54 45.54 0 1 1 0-91.08 45.54 45.54 0 0 1 0 91.08z"
              />
              <filter
                id="a"
                width="140.6%"
                height="140.6%"
                x="-20.3%"
                y="-15.9%"
                filterUnits="objectBoundingBox"
              >
                <feOffset dy="4" in="SourceAlpha" result="shadowOffsetOuter1" />
                <feGaussianBlur
                  in="shadowOffsetOuter1"
                  result="shadowBlurOuter1"
                  stdDeviation="5.5"
                />
                <feColorMatrix
                  in="shadowBlurOuter1"
                  result="shadowMatrixOuter1"
                  values="0 0 0 0 0.145098039 0 0 0 0 0.17254902 0 0 0 0 0.380392157 0 0 0 0.15 0"
                />
                <feOffset dy="2" in="SourceAlpha" result="shadowOffsetOuter2" />
                <feGaussianBlur
                  in="shadowOffsetOuter2"
                  result="shadowBlurOuter2"
                  stdDeviation="1.5"
                />
                <feColorMatrix
                  in="shadowBlurOuter2"
                  result="shadowMatrixOuter2"
                  values="0 0 0 0 0.364705882 0 0 0 0 0.392156863 0 0 0 0 0.580392157 0 0 0 0.2 0"
                />
                <feMerge>
                  <feMergeNode in="shadowMatrixOuter1" />
                  <feMergeNode in="shadowMatrixOuter2" />
                </feMerge>
              </filter>
            </defs>
            <g fill="none" fill-rule="evenodd">
              <circle
                cx="68.85"
                cy="68.85"
                r="68.85"
                fill="#5468FF"
                opacity=".07"
              />
              <circle
                cx="68.85"
                cy="68.85"
                r="52.95"
                fill="#5468FF"
                opacity=".08"
              />
              <use fill="#000" filter="url(#a)" xlink:href="#b" />
              <use fill="url(#c)" xlink:href="#b" />
              <path
                d="M76.01 75.44c5-5 5.03-13.06.07-18.01a12.73 12.73 0 0 0-18 .07c-5 4.99-5.03 13.05-.07 18a12.73 12.73 0 0 0 18-.06zm2.5 2.5a16.28 16.28 0 0 1-23.02.09A16.29 16.29 0 0 1 55.57 55a16.28 16.28 0 0 1 23.03-.1 16.28 16.28 0 0 1-.08 23.04zm1.08-1.08l-2.15 2.16 8.6 8.6 2.16-2.15-8.6-8.6z"
                fill="#5369FF"
              />
            </g>
          </svg>
          <p class="mt-2">Sorry, we can't find any matches to your query!</p>
          <p>Please try another query.</p>
        </div>
      </template>
    </div>
    <div class="col-md-4">
      <iq-card>
        <template v-slot:body>
          <div class="iq-todo-right">
            <form class="position-relative">
              <div class="form-group mb-0">
                <input
                  type="text"
                  class="form-control todo-search"
                  id="exampleInputEmail001"
                  placeholder="Search"
                />
                <a class="search-link" href="#">
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
                </a>
              </div>
            </form>
            <div class="iq-todo-friendlist mt-3">
              <ul class="suggestions-lists m-0 p-0">
                <li
                  class="d-flex mb-4 align-items-center"
                  v-for="(item, index) in friendList"
                  :key="index"
                >
                  <div class="user-img img-fluid">
                    <img
                      :src="item.img"
                      alt="story-img"
                      class="rounded-circle avatar-40"
                    />
                  </div>
                  <div
                    class="d-flex align-items-center justify-content-between w-100"
                  >
                    <div class="ms-3">
                      <h6>{{ item.name }}</h6>
                      <p class="mb-0">{{ item.work }}</p>
                    </div>
                    <div class="card-header-toolbar d-flex align-items-center">
                      <div class="dropdown">
                        <span
                          class="dropdown-toggle"
                          id="dropdownMenuButton41"
                          data-bs-toggle="dropdown"
                          aria-expanded="false"
                        >
                          <i class="material-symbols-outlined md-18"
                            >more_vert</i
                          >
                        </span>
                        <div class="dropdown-menu dropdown-menu-right" style="">
                          <a
                            class="dropdown-item d-flex align-items-center"
                            href="#"
                            ><i class="material-symbols-outlined me-2 md-18"
                              >person</i
                            >Unfollow</a
                          >
                          <a
                            class="dropdown-item d-flex align-items-center"
                            href="#"
                            ><i class="material-symbols-outlined me-2 md-18"
                              >cancel</i
                            >Unfriend</a
                          >
                          <a
                            class="dropdown-item d-flex align-items-center"
                            href="#"
                            ><i class="material-symbols-outlined me-2 md-18"
                              >lock</i
                            >block</a
                          >
                        </div>
                      </div>
                    </div>
                  </div>
                </li>
              </ul>
              <a
                href="#"
                class="btn btn-primary d-flex align-items-center justify-content-center"
                ><i class="material-symbols-outlined md-18 me-1">add</i> Load
                More</a
              >
            </div>
          </div>
        </template>
      </iq-card>
    </div>
  </div>
</template>
<script setup>
import { defineProps } from "vue";

import TaskForm from "./TaskForm";

defineProps({
  taskList: { type: Array, default: () => [] },
  categoryList: { type: Array, default: () => [] },
  category: { type: Object, default: () => {} },
  project: { type: Object, default: () => {} },
});

const Users = [
  {
    id: 1,
    name: "Danlel Cllfferton",
    role: "Lorem Ipsum is",
    isPrivate: true,
    image: require("@/assets/images/user/01.jpg"),
    isActive: true,
  },
  {
    id: 2,
    name: "Cralg Danles",
    role: "There are many ",
    image: require("@/assets/images/user/02.jpg"),
    isActive: false,
  },
  {
    id: 3,
    name: "Simona Gomez",
    role: "This Sunday we",
    isPrivate: true,
    image: require("@/assets/images/user/03.jpg"),
    isActive: true,
  },
  {
    id: 4,
    name: "Serena Gemoz",
    role: "passages of Lorem",
    image: require("@/assets/images/user/04.jpg"),
    isActive: true,
  },
  {
    id: 5,
    name: "Jeena Gaze",
    role: "Lorem Ipsum used",
    image: require("@/assets/images/user/05.jpg"),
    isActive: false,
  },
  {
    id: 6,
    name: "migule Slimmonas",
    role: "translation by",
    image: require("@/assets/images/user/06.jpg"),
    isActive: true,
  },
  {
    id: 7,
    name: "Becky Dimes",
    role: "Lorem Ipsum which",
    image: require("@/assets/images/user/07.jpg"),
    isActive: false,
  },
  {
    id: 8,
    name: "James Romero",
    role: "simply random text",
    image: require("@/assets/images/user/06.jpg"),
    isActive: true,
  },
  {
    id: 9,
    name: "Maya Didas",
    role: " but also the leap",
    image: require("@/assets/images/user/07.jpg"),
    isActive: false,
  },
  {
    id: 10,
    name: "Monty Carlo",
    role: "Contrary to popular",
    image: require("@/assets/images/user/08.jpg"),
    isActive: true,
  },
];

// import { mapGetters } from "vuex";
const checkUser = (item, type) => {
  const user = Users.find((user) => user.id === item);
  let final;
  if (user !== undefined) {
    switch (type) {
      case "name":
        final = user.name;
        break;
      case "image":
        final = user.image;
        break;
      case "role":
        final = user.role;
        break;
    }
    return final;
  }
  return false;
};
const friendList = [
  {
    img: require("../../../assets/images/user/01.jpg"),
    name: "Paul Molive",
    work: "trainee",
  },
  {
    img: require("../../../assets/images/user/02.jpg"),
    name: "Anna Mull",
    work: "Web Developer",
  },
  {
    img: require("../../../assets/images/user/03.jpg"),
    name: "Paige Turner",
    work: "trainee",
  },
  {
    img: require("../../../assets/images/user/04.jpg"),
    name: "Barb Ackue",
    work: "Web Designer",
  },
  {
    img: require("../../../assets/images/user/05.jpg"),
    name: "Greta Life",
    work: "Tester",
  },
  {
    img: require("../../../assets/images/user/06.jpg"),
    name: "Ira Membrit",
    work: "Android Developer",
  },
  {
    img: require("../../../assets/images/user/07.jpg"),
    name: "Pete Sariya",
    work: "Web Designer",
  },
];
</script>
