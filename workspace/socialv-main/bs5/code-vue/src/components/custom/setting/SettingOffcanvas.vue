<template>
  <!-- Setting offcanvas start here -->
  <b-offcanvas
    v-model="show"
    :backdrop="false"
    title=""
    :placement="themeSchemeDirection !== 'ltr' ? 'start' : 'end'"
    class="live-customizer"
    header-class="pb-0"
    id="live-customizer"
    :body-scrolling="true"
  >
    <template #title>
      <h4 class="d-flex align-items-center">Setting Panel</h4>
    </template>
    <div class="row">
      <div class="col-lg-12">
        <div>
          <div class="text-center mb-4">
            <h5 class="d-inline-block">Style Setting</h5>
          </div>
          <div>
            <!-- Theme start here -->
            <theme-scheme />
            <!-- Theme end here -->
            <hr />
            <!-- Menu Style start here -->
            <menu-style v-if="isShowSetting('isSidebar')" />
            <!-- Menu Style end here -->
            <hr />
            <!-- Active Menu Style start here -->
            <menu-active-style v-if="isShowSetting('isSidebar')" />
            <!-- Active Menu Style end here -->
            <hr />
            <!-- Color customizer start here -->
            <color-customizer />
            <!-- Color customizer end here -->
            <hr />
            <direction />
          </div>
        </div>
      </div>
    </div>
  </b-offcanvas>
  <a
    class="btn btn-fixed-end btn-danger btn-icon btn-setting"
    id="settingbutton"
    role="button"
    @click="open"
  >
    <span class="icon material-symbols-outlined animated-rotate text-white">
      settings
    </span>
  </a>
  <!-- Settings sidebar end here -->
</template>
<script>
// Vue / Vuex Functions
import { ref, onMounted, onUnmounted, computed, watch } from "vue";
import { useSetting } from "../../../store/pinia";
import { useRoute } from "vue-router";

// Style Components
import ThemeScheme from "./sections/ThemeScheme.vue";
import ColorCustomizer from "./sections/ColorCustomizer.vue";
import MenuStyle from "./sections/MenuStyle.vue";
import MenuActiveStyle from "./sections/MenuActiveStyle.vue";
import Direction from "./sections/Direction.vue";

export default {
  name: "SettingOffcanvas",
  components: {
    // Style Components
    ThemeScheme,
    ColorCustomizer,
    MenuStyle,
    MenuActiveStyle,
    Direction,
  },
  setup() {
    // Store objects
    const store = useSetting();
    const route = useRoute();
    const themeSchemeDirection = computed(
      () => store.theme_scheme_direction_custom,
    );

    // Variables
    const show = ref(false);

    // Functions
    const close = () => {
      show.value = false;
    };
    const open = () => {
      show.value = true;
    };
    const onClick = (e) => {
      if (show.value) {
        if (
          e.target.closest(".live-customizer") == null &&
          e.target.closest("#settingbutton") == null
        ) {
          show.value = false;
        }
      }
    };
    const defaultSetting = () => {
      store.dispatch("setting/reset_state");
    };
    const isShowSetting = (name) => {
      return !route.meta[name];
    };
    const addOffcanvasDismiss = () => {
      const els = document.querySelectorAll(".text-reset");
      for (let i = 0; i < els.length; i++) {
        els[i].setAttribute("data-bs-dismiss", "offcanvas");
      }
    };
    // Life cycle hooks
    watch(themeSchemeDirection, () => {
      show.value = false;
    });
    onMounted(() => {
      document.body.addEventListener("click", onClick);
      addOffcanvasDismiss();
    });
    onUnmounted(() => {
      document.body.removeEventListener("click", onClick);
    });

    // Return functions & variables
    return {
      themeSchemeDirection,
      show,
      isShowSetting,
      defaultSetting,
      close,
      open,
    };
  },
};
</script>
<style>
.live-customizer .offcanvas-title {
  font-size: calc(1.269rem + 0.228vw);
  flex: 1;
}

@media (min-width: 1200px) {
  .live-customizer .offcanvas-title {
    font-size: 1.44rem;
  }
}
</style>
