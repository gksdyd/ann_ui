<template>
  <div class="btn-group iq-qty-btn" data-qty="btn" role="group">
    <button type="button" class="minus me-2" v-on:click.prevent="decrement">-
    </button>
    <input type="text" class="btn btn-sm input-text qty text input-display " v-model="newValue" data-qty="input"
      title="Qty" readonly="" />
    <button type="button" class="plus ms-1" v-on:click.prevent="increment">+
    </button>
  </div>
</template>

<script>
import { ref, watch } from "vue";
export default {
  props: {
    modelValue: {
      type: Number,
      default: 1,
    },
  },
  methods: {
    increment() {
      this.newValue++;
    },
    decrement() {
      if (this.newValue <= 0) {
        this.newValue = 0;
      } else {
        this.newValue--;
      }
    },
  },
  emits: ["update:modelValue"],
  setup(props, { emit }) {
    const newValue = ref(props.modelValue);
    watch(newValue, () => {
      emit("update:modelValue", newValue.value);
    });
    return {
      newValue,
    };
  },
};
</script>
