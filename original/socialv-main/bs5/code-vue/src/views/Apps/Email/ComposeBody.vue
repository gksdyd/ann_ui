<template>
  <b-card no-body class="iq-border-radius-20">
    <b-card-body>
      <b-row>
        <b-col md="12" class="mb-3">
          <h5 class="text-primary card-title d-flex gap-1">
            <span class="material-symbols-outlined"
              >drive_file_rename_outline</span
            >
            Compose Message
          </h5>
          <button
            type="submit"
            class="float-end close-popup"
            v-if="modal"
            @click="close"
            data-dismiss="modal"
          >
            <i class="ri-close-fill"></i>
          </button>
        </b-col>
      </b-row>
      <form class="email-form">
        <b-row class="form-group">
          <label for="inputEmail3" class="col-sm-2 col-form-label">To:</label>
          <b-col sm="10">
            <multi-select
              class="select2jsMultiSelect mb-0"
              id="inputEmail3"
              :options="[
                'Petey Cruiser',
                'Bob Frapples',
                'Barb Ackue',
                'Greta Life',
              ]"
              :create-new="true"
              :is-required="true"
            ></multi-select>
          </b-col>
        </b-row>
        <b-row class="form-group">
          <label for="cc" class="col-sm-2 col-form-label">Cc:</label>
          <b-col sm="10">
            <multi-select
              class="select2jsMultiSelect mb-0"
              id="inputEmail3"
              :options="[
                'Brock Lee',
                `Rick O'Shea`,
                'Cliff Hanger',
                'Barb Dwyer',
              ]"
              :create-new="true"
              :is-required="true"
            ></multi-select>
          </b-col>
        </b-row>
        <b-row class="form-group">
          <label for="subject" class="col-sm-2 col-form-label">Subject:</label>
          <b-col sm="10">
            <input type="text" id="subject" class="form-control" />
          </b-col>
        </b-row>
        <b-row class="form-group">
          <label for="subject" class="col-sm-2 col-form-label"
            >Your Message:</label
          >
          <b-col md="10">
            <textarea class="textarea form-control" rows="5">
Next, use our Get Started docs to setup Tiny!</textarea
            >
          </b-col>
        </b-row>
        <div
          class="form-group d-flex justify-content-between align-items-center compose-bottom pt-3 m-0"
        >
          <div class="d-flex flex-wrap flex-grow-1 align-items-center">
            <div class="send-btn">
              <button type="submit" class="btn btn-primary">Send</button>
            </div>
            <div class="send-panel">
              <label class="ms-2 mb-0 bg-primary-subtle rounded" for="file">
                <input type="file" id="file" style="display: none" />
                <a
                  href="#"
                  class="material-symbols-outlined writ-icon text-primary"
                >
                  attachment
                </a>
              </label>
              {{ "" }}
              <label class="ms-2 mb-0 bg-primary-subtle rounded">
                <a href="#" class="material-symbols-outlined text-primary">
                  place
                </a>
              </label>
              {{ "" }}
              <label class="ms-2 mb-0 bg-primary-subtle rounded">
                <a href="#" class="material-symbols-outlined text-primary">
                  add_to_drive
                </a>
              </label>
              {{ "" }}
              <label class="ms-2 mb-0 bg-primary-subtle rounded">
                <a href="#" class="material-symbols-outlined text-primary">
                  photo_camera
                </a>
              </label>
              {{ "" }}
              <label class="ms-2 mb-0 bg-primary-subtle rounded">
                <a href="#" class="material-symbols-outlined text-primary">
                  sentiment_satisfied
                </a>
              </label>
            </div>
          </div>
          <div class="d-flex align-items-center">
            <div class="send-panel float-right">
              <label class="ms-2 mb-0 bg-primary-subtle rounded"
                ><a href="#" class="material-symbols-outlined text-primary">
                  settings
                </a></label
              >
              {{ "" }}
              <label class="ms-2 mb-0 bg-primary-subtle rounded"
                ><a href="#" class="material-symbols-outlined"> delete </a>
              </label>
            </div>
          </div>
        </div>
      </form>
    </b-card-body>
  </b-card>
</template>
<script>
import multiSelect from "../../../components/MultiSelect.vue";
export default {
  name: "ComposeBody",
  components: {
    multiSelect,
  },
  props: {
    modal: { type: Boolean, default: false },
  },
  data() {
    return {
      singleSelect: "",
      singleSelect1: "",
      singleOption: [
        { id: 1, text: "Java" },
        { id: 2, text: "PHP" },
        { id: 3, text: "JavaScript" },
        { id: 4, text: "Visual Basics" },
      ],
      singleOption1: [
        { id: 1, text: "Red" },
        { id: 2, text: "Green" },
        { id: 3, text: "Blue" },
        { id: 4, text: "Yellow" },
      ],
    };
  },
  methods: {
    close() {
      this.$emit("close", false);
    },
  },
};
</script>
