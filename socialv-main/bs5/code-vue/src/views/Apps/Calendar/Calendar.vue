<template>
  <div class="content-inner">
    <div class="container">
      <div class="row row-eq-height">
        <div class="col-md-4 col-lg-4">
          <div class="card">
            <div class="card-body text-center">
              <flat-picker
                v-model="inlineDate"
                className="d-none"
                :config="inlineDatepicker"
                placeholder="select Date"
              ></flat-picker>
            </div>
          </div>
          <b-card no-body>
            <div class="card-header d-flex justify-content-between">
              <div class="header-title">
                <h4 class="card-title">Classification</h4>
              </div>
              <div class="card-header-toolbar d-flex align-items-center">
                <a href="#" class="material-symbols-outlined"> add </a>
              </div>
            </div>
            <b-card-body class="pt-0">
              <ul class="m-0 p-0 job-classification list-inline">
                <li class="d-flex align-items-center">
                  <i class="material-symbols-outlined md-18 bg-primary"
                    >check_circle</i
                  >Meeting
                </li>
                <li class="d-flex align-items-center">
                  <i class="material-symbols-outlined md-18 bg-success"
                    >check_circle</i
                  >Business travel
                </li>
                <li class="d-flex align-items-center">
                  <i class="material-symbols-outlined md-18 bg-warning"
                    >check_circle</i
                  >Personal Work
                </li>
                <li class="d-flex align-items-center">
                  <i class="material-symbols-outlined md-18 bg-info"
                    >check_circle</i
                  >Team Project
                </li>
              </ul>
            </b-card-body>
          </b-card>
          <b-card no-body>
            <div class="card-header d-flex justify-content-between">
              <div class="header-title">
                <h4 class="card-title">Today's Schedule</h4>
              </div>
            </div>
            <b-card-body class="pt-0">
              <ul class="m-0 p-0 today-schedule">
                <li class="d-flex">
                  <div class="schedule-icon">
                    <i class="material-symbols-outlined text-primary md-18"
                      >fiber_manual_record</i
                    >
                  </div>
                  <div class="schedule-text">
                    <span>Web Design</span>
                    <span>09:00 to 12:00</span>
                  </div>
                </li>
                <li class="d-flex">
                  <div class="schedule-icon">
                    <i class="material-symbols-outlined text-success md-18"
                      >fiber_manual_record</i
                    >
                  </div>
                  <div class="schedule-text">
                    <span>Participate in Design</span>
                    <span>09:00 to 12:00</span>
                  </div>
                </li>
              </ul>
            </b-card-body>
          </b-card>
        </div>
        <div class="col-md-8 col-lg-8">
          <div class="card">
            <div class="card-header d-flex justify-content-between flex-wrap">
              <div class="header-title">
                <h4 class="card-title">Book Appointment</h4>
              </div>
              <div
                class="card-header-toolbar d-flex align-items-center mt-1 mt-md-0"
              >
                <a href="#" class="btn btn-primary d-flex align-items-center"
                  ><i class="material-symbols-outlined me-1 md-18">add</i>Book
                  Appointment</a
                >
              </div>
            </div>
            <div class="card body pt-0 mb-0">
              <div class="card card-block card-stretch mb-0">
                <div class="card-body pt-0">
                  <div id="calendar1" class="calendar-s"></div>
                  <full-calender :events="events"></full-calender>
                </div>
              </div>
            </div>
          </div>
        </div>
        <modal
          id="modalcal"
          tabindex="-1"
          title="Create Post"
          aria-labelledby="modalcalLabel"
          aria-hidden="true"
        >
          <model-header>
            <h5 class="modal-title" id="modalcalLabel">Add New Event</h5>
            <button
              :dismissable="true"
              type="button"
              class="btn-close"
              data-bs-dismiss="modal"
            ></button>
          </model-header>
          <model-body>
            <div class="row">
              <div class="col-md-12 mb-3">
                <label
                  for="Text1"
                  class="form-label font-weight-bold text-muted text-uppercase"
                  >Event Title</label
                >
                <input
                  type="text"
                  class="form-control"
                  id="Text1"
                  placeholder="Enter Event Title"
                />
              </div>
              <div class="col-md-12">
                <label
                  for="Text5"
                  class="form-label font-weight-bold text-muted text-uppercase"
                  >Date & Time</label
                >
              </div>
              <div class="col-md-6 mb-3">
                <div class="input-group">
                  <input
                    type="text"
                    class="form-control vanila-datepicker"
                    name="range-start"
                    placeholder="Start Date"
                  />
                  <div class="input-group-append">
                    <span class="input-group-text">
                      <svg
                        xmlns="http://www.w3.org/2000/svg"
                        class=""
                        width="18"
                        fill="none"
                        viewBox="0 0 24 24"
                        stroke="currentColor"
                      >
                        <path
                          stroke-linecap="round"
                          stroke-linejoin="round"
                          stroke-width="2"
                          d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z"
                        />
                      </svg>
                    </span>
                  </div>
                </div>
              </div>
              <div class="col-md-6 mb-3">
                <div class="input-group">
                  <input
                    type="text"
                    class="form-control vanila-datepicker"
                    name="range-end"
                    placeholder="End Date"
                  />
                  <div class="input-group-append" style="user-select: auto">
                    <span class="input-group-text" style="user-select: auto">
                      <svg
                        xmlns="http://www.w3.org/2000/svg"
                        class=""
                        width="18"
                        fill="none"
                        viewBox="0 0 24 24"
                        stroke="currentColor"
                        style="user-select: auto"
                      >
                        <path
                          stroke-linecap="round"
                          stroke-linejoin="round"
                          stroke-width="2"
                          d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z"
                          style="user-select: auto"
                        ></path>
                      </svg>
                    </span>
                  </div>
                </div>
              </div>
              <div class="col-md-12 mb-3">
                <div class="form-check form-check-inline">
                  <div
                    class="custom-control custom-checkbox custom-control-inline"
                  >
                    <input
                      type="checkbox"
                      class="custom-control-input m-0"
                      id="inlineCheckbox1"
                    />
                    <label class="custom-control-label" for="inlineCheckbox1"
                      >All Day</label
                    >
                  </div>
                </div>
                <div class="form-check form-check-inline">
                  <div
                    class="custom-control custom-checkbox custom-control-inline"
                  >
                    <input
                      type="checkbox"
                      class="custom-control-input m-0"
                      id="inlineCheckbox2"
                      checked
                    />
                    <label class="custom-control-label" for="inlineCheckbox2"
                      >Does not repeat</label
                    >
                  </div>
                </div>
              </div>
              <div class="col-md-12 mb-3">
                <label
                  for="inputState"
                  class="form-label font-weight-bold text-muted text-uppercase"
                  >Category</label
                >
                <select
                  id="inputState"
                  class="form-select form-control choicesjs"
                >
                  <option selected="">Select Category</option>
                  <option>Appointments</option>
                  <option>Birthday</option>
                  <option>Meetings</option>
                  <option>Tour</option>
                  <option>Anniversary</option>
                </select>
              </div>
              <div class="col-md-12 mb-3">
                <label
                  for="Text9"
                  class="form-label font-weight-bold text-muted text-uppercase"
                  >Description</label
                >
                <textarea
                  class="form-control"
                  id="Text9"
                  rows="2"
                  placeholder="Enter Description"
                ></textarea>
              </div>
            </div>
            <div class="d-flex justify-content-end">
              <button type="button" class="btn btn-primary">Add Event</button>
            </div>
          </model-body>
        </modal>
      </div>
    </div>
  </div>
</template>
<script setup>
import { ref, reactive } from "vue";
import moment from "moment";
import FullCalender from "@/components/custom/calender/FullCalender.vue";
import FlatPicker from "vue-flatpickr-component";
import "flatpickr/dist/flatpickr.css";

const inlineDate = ref("");

const inlineDatepicker = reactive({
  inline: true,
  minDate: "today",
  dateFormat: "Y-m-d",
});
const account = ref({
  series: [
    {
      name: "Total Account",
      data: [42, 30, 25, 40, 57, 71, 86, 71, 108],
    },
  ],
  options: {
    colors: ["#50b5ff"],
    chart: {
      toolbar: {
        show: false,
      },
    },
    forecastDataPoints: {
      count: 2,
    },
    stroke: {
      width: 3,
    },
    grid: {
      show: true,
      strokeDashArray: 7,
    },
    markers: {
      size: 6,
      colors: "#FFFFFF",
      strokeColors: ["#50b5ff"],
      strokeWidth: 2,
      strokeOpacity: 0.9,
      strokeDashArray: 0,
      fillOpacity: 0,
      shape: "circle",
      radius: 2,
      offsetX: 0,
      offsetY: 0,
    },
    xaxis: {
      categories: [
        "Jan",
        "Feb",
        "Mar",
        "Apr",
        "May",
        "Jun",
        "Jul",
        "Aug",
        "Sep",
      ],
      axisBorder: {
        show: false,
      },
      axisTicks: {
        show: false,
      },
      tooltip: {
        enabled: false,
      },
    },
  },
});

const events = ref([
  {
    title: "5:30a Click for Google",
    url: "http://google.com/",
    start: moment(new Date(), "YYYY-MM-DD")
      .add(-20, "days")
      .format("YYYY-MM-DD"),
    color: "#50b5ff",
  },
  {
    title: "5:30a All Day Event",
    start: moment(new Date(), "YYYY-MM-DD")
      .add(-18, "days")
      .format("YYYY-MM-DD"),
    color: "#a09e9e",
  },
  {
    title: "5:30a Long Event",
    start: moment(new Date(), "YYYY-MM-DD")
      .add(-16, "days")
      .format("YYYY-MM-DD"),
    end: moment(new Date(), "YYYY-MM-DD").add(-13, "days").format("YYYY-MM-DD"),
    color: "#49f0d3",
  },
  {
    groupId: "999",
    title: "5:30a Repeating Event",
    start: moment(new Date(), "YYYY-MM-DD")
      .add(-14, "days")
      .format("YYYY-MM-DD"),
    color: "#ffba68",
  },
  {
    groupId: "999",
    title: "5:30a Repeating Event",
    start: moment(new Date(), "YYYY-MM-DD")
      .add(-12, "days")
      .format("YYYY-MM-DD"),
    color: "#d592ff ",
  },
  {
    groupId: "999",
    title: "5:30a Repeating Event",
    start: moment(new Date(), "YYYY-MM-DD")
      .add(-10, "days")
      .format("YYYY-MM-DD"),
    color: "#ff9b8a",
  },
  {
    title: "5:30a Birthday Party",
    start: moment(new Date(), "YYYY-MM-DD")
      .add(-8, "days")
      .format("YYYY-MM-DD"),
    color: "#49f0d3",
  },
  {
    title: " Meeting",
    start: moment(new Date(), "YYYY-MM-DD")
      .add(-6, "days")
      .format("YYYY-MM-DD"),
    color: "#a09e9e",
  },
  {
    title: "5:30a Birthday Party",
    start: moment(new Date(), "YYYY-MM-DD")
      .add(-5, "days")
      .format("YYYY-MM-DD"),
    color: "#49f0d3",
  },
  {
    title: "5:30a Birthday Party",
    start: moment(new Date(), "YYYY-MM-DD")
      .add(-2, "days")
      .format("YYYY-MM-DD"),
    color: "#ff9b8a ",
  },

  {
    title: "5:30a Meeting",
    start: moment(new Date(), "YYYY-MM-DD").add(0, "days").format("YYYY-MM-DD"),
    color: "#ff9b8a",
  },
  {
    title: "6:30a Click for Google",
    url: "http://google.com/",
    start: moment(new Date(), "YYYY-MM-DD").add(0, "days").format("YYYY-MM-DD"),
    color: "#d592ff",
  },
  {
    groupId: "999",
    title: "7:30a Repeating Event",
    start: moment(new Date(), "YYYY-MM-DD").add(0, "days").format("YYYY-MM-DD"),
    color: "#49f0d3",
  },
  {
    title: "8:30a Birthday Party",
    start: moment(new Date(), "YYYY-MM-DD").add(0, "days").format("YYYY-MM-DD"),
    color: "#f4a965",
  },
  {
    title: "Doctor Meeting",
    start: moment(new Date(), "YYYY-MM-DD").add(0, "days").format("YYYY-MM-DD"),
    color: "#f4a965",
  },
  {
    title: "5:30a All Day Event",
    start: moment(new Date(), "YYYY-MM-DD").add(1, "days").format("YYYY-MM-DD"),
    color: " #50b5ff",
  },
  {
    groupId: "999",
    title: "5:30a Repeating Event",
    start: moment(new Date(), "YYYY-MM-DD").add(8, "days").format("YYYY-MM-DD"),
    color: " #50b5ff",
  },
  {
    groupId: "999",
    title: "5:30a Repeating Event",
    start: moment(new Date(), "YYYY-MM-DD")
      .add(10, "days")
      .format("YYYY-MM-DD"),
    color: "#49f0d3",
  },
]);
</script>
<style>
.flatpickr-calendar {
  width: 100%;
}

[data-bs-theme="dark"] .flatpickr-calendar {
  background-color: var(--bs-gray-900) !important;
  color: var(--bs-heading-color) !important;
}

[data-bs-theme="dark"] .flatpickr-month,
.flatpickr-weekday,
.flatpickr-day {
  color: var(--bs-heading-color) !important;
}

[data-bs-theme="dark"] .flatpickr-disabled,
.nextMonthDay {
  color: #7a7a7a !important;
}

.flatpickr-calendar.inline{
  margin-left: calc(var(--bs-border-width) * -1) !important;
}
</style>
