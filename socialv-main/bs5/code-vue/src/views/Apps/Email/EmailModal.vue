<template>
  <b-modal
    id="compose-email-popup"
    size="lg"
    title="Compose Message"
    centered
    hide-footer
    titleClass="las la-pen text-primary"
  >
    <form @submit.prevent="sendEmail">
      <div class="form-group row">
        <label for="inputEmail3" class="col-sm-2 col-form-label">To:</label>
        <div class="col-sm-10">
          <b-form-input v-model="to" id="inputEmail3"></b-form-input>
        </div>
      </div>
      <div class="form-group row">
        <label for="cc" class="col-sm-2 col-form-label">Cc:</label>
        <div class="col-sm-10">
          <b-form-input v-model="cc" id="cc" z></b-form-input>
        </div>
      </div>
      <div class="form-group row">
        <label for="subject" class="col-sm-2 col-form-label">Subject:</label>
        <div class="col-sm-10">
          <input
            v-model="subject"
            type="text"
            id="subject"
            class="form-control"
          />
        </div>
      </div>
      <div class="form-group row">
        <label for="message" class="col-sm-2 col-form-label"
          >Your Message:
        </label>
        <div class="col-sm-10">
          <b-form-textarea
            v-model="message"
            id="message"
            rows="5"
            placeholder="Next, use our Get Started docs to setup Tiny!"
          ></b-form-textarea>
        </div>
      </div>
      <div
        class="form-group d-flex justify-content-between align-items-center compose-bottom pt-3 m-0"
      >
        <div class="d-flex flex-grow-1 align-items-center">
          <div class="send-btn">
            <button type="submit" class="btn btn-primary">Send</button>
          </div>
          <div class="send-panel">
            <label class="ms-2 mb-0 bg-primary-subtle rounded" for="file">
              <input type="file" id="file" style="display: none" />
              <a
                href="#"
                class="material-symbols-outlined writ-icon text-primary"
                >attachment</a
              >
            </label>
            <label class="ms-2 mb-0 bg-primary-subtle rounded">
              <a href="#" class="material-symbols-outlined text-primary"
                >place</a
              >
            </label>
            <label class="ms-2 mb-0 bg-primary-subtle rounded">
              <a href="#" class="material-symbols-outlined text-primary"
                >add_to_drive</a
              >
            </label>
            <label class="ms-2 mb-0 bg-primary-subtle rounded">
              <a href="#" class="material-symbols-outlined text-primary"
                >photo_camera</a
              >
            </label>
            <label class="ms-2 mb-0 bg-primary-subtle rounded">
              <a href="#" class="material-symbols-outlined text-primary"
                >sentiment_satisfied</a
              >
            </label>
          </div>
        </div>
        <div class="d-flex align-items-center">
          <div class="send-panel float-right">
            <label class="ms-2 mb-0 bg-primary-subtle rounded">
              <a href="#" class="material-symbols-outlined text-primary"
                >settings</a
              >
            </label>
            <label class="ms-2 mb-0 bg-primary-subtle rounded">
              <a href="#" class="material-symbols-outlined">delete</a>
            </label>
          </div>
        </div>
      </div>
    </form>
  </b-modal>
</template>

<script>
export default {
  data() {
    return {
      to: null,
      cc: null,
      subject: "",
      message: "",
    };
  },

  methods: {
    addDataDismiss() {
      var els = document.querySelectorAll(".btn-close");
      for (var i = 0; i < els.length; i++) {
        els[i].setAttribute("data-bs-dismiss", "modal");
      }
    },
  },
  mounted() {
    // Call addDataDismiss when the component is mounted
    this.addDataDismiss();
  },
};
</script>

<style>
/* Media Query for Small Devices */
@media (max-width: 767.98px) {
  .send-panel {
    display: flex;
    flex-wrap: wrap;
  }
  .send-panel label {
    margin-right: 5px;
    margin-bottom: 5px;
  }
}
</style>
