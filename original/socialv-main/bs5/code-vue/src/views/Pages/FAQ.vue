<template>
  <div class="content-inner">
    <b-container>
      <b-row>
        <b-col sm="12">
          <div
            class="card position-relative inner-page-bg bg-primary"
            style="height: 150px"
          >
            <div class="inner-page-title">
              <h3 class="text-white">FAQ Page</h3>
              <p class="text-white">lorem ipsum</p>
            </div>
          </div>
        </b-col>
        <div id="faqAccordion" class="container">
          <b-col lg="12">
            <div class="accordion" id="accordionExample">
              <div
                class="accordion-item mb-3"
                v-for="(item, index) in faqList"
                :key="index"
              >
                <h2 class="accordion-header" id="heading1">
                  <button
                    :class="
                      item.active
                        ? 'accordion-button'
                        : 'accordion-button collapsed'
                    "
                    type="button"
                    data-bs-toggle="collapse"
                    :data-bs-target="'#collapse' + index"
                    aria-expanded="false"
                    :aria-controls="'collapse' + index"
                  >
                    {{ item.title }}
                  </button>
                </h2>
                <div
                  :id="'collapse' + index"
                  :class="
                    item.active
                      ? 'accordion-collapse collapse show'
                      : 'accordion-collapse collapse'
                  "
                  aria-labelledby="heading1"
                  data-bs-parent="#accordionExample"
                >
                  <div class="accordion-body">
                    <p>{{ item.description }}</p>
                  </div>
                </div>
              </div>
            </div>
          </b-col>
        </div>
      </b-row>
    </b-container>
  </div>
</template>
<script>
// import { socialvue } from '../../config/pluginInit'

export default {
  name: "FAQ",
  mounted() {
    // socialvue.index()
  },
  data() {
    return {
      faqList: [
        {
          title: "It is a long established reader will be?",
          description:
            "Many desktop publishing packages and web page editors now use Lorem Ipsum as their default model text, and a search for 'lorem ipsum' will uncover many web sites still in their infancy.",
          active: true,
        },
        {
          title: "Distracted by the readable page whent?",
          description:
            "It has survived not only five centuries, but also the leap into electronic typesetting. Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur.",
        },
        {
          title: "What is user interface kit?",
          description:
            "It has survived not only five centuries, but also the leap into electronic typesetting. Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur.",
        },
        {
          title: "The readable content layout?",
          description:
            "It has survived not only five centuries, but also the leap into electronic typesetting. Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur.",
        },
        {
          title: "The readable content of a page at its layout?",
          description:
            "It has survived not only five centuries, but also the leap into electronic typesetting. Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur.",
        },
        {
          title: "What is user interface kit?",
          description:
            "It has survived not only five centuries, but also the leap into electronic typesetting. Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur.",
        },
        {
          title: "The readable content and survived?",
          description:
            "It has survived not only five centuries, but also the leap into electronic typesetting. Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur.",
        },
        {
          title: "The readable content of a page layout?",
          description:
            "It has survived not only five centuries, but also the leap into electronic typesetting. Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur.",
        },
        {
          title: "Distracted by readable content of a page?",
          description:
            "It has survived not only five centuries, but also the leap into electronic typesetting. Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur.",
        },
      ],
    };
  },
};
</script>
