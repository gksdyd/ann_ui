<template>
  <div class="btn-group iq-qty-btn" data-qty="btn" role="group">
    <button
      type="button"
      class="btn btn-outline-light iq-quantity-minus text-dark"
      v-on:click.prevent="decrement"
    >
      -
    </button>
    <input
      type="text"
      class="btn btn-outline-light input-display"
      v-model="newValue"
      data-qty="input"
      title="Qty"
      readonly=""
    />
    <button
      type="button"
      class="btn btn-outline-light iq-quantity-plus text-dark"
      v-on:click.prevent="increment"
    >
      +
    </button>
  </div>
</template>

<script>
import { ref, watch } from "vue";
export default {
  props: {
    modelValue: {
      type: Number,
      default: 2,
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
