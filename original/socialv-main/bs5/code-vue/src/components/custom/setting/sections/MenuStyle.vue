<template>
  <div>
    <h5 class="mt-4 mb-3">Menu Style</h5>
    <div class="d-grid gap-3 grid-cols-3 mb-4">
      <checkbox-input btn-name="sidebar_type" :imgComponent="true" label-title="Mini" id="sidebar-mini"
        :default-checked="menuStyle" value="sidebar-mini" @onChange="store.sidebar_type">
        Mini
      </checkbox-input>
      <checkbox-input btn-name="sidebar_type" :imgComponent="true" label-title="Hover" id="sidebar-hover"
        :default-checked="menuStyle" value="sidebar-hover" @onChange="store.sidebar_type">
        Hover
      </checkbox-input>
      <checkbox-input btn-name="sidebar_type" :imgComponent="true" label-title="Hover" id="sidebar-soft"
        :default-checked="menuStyle" value="sidebar-soft" @onChange="store.sidebar_type">
        Soft
      </checkbox-input>
    </div>
  </div>
</template>
<script setup>
import { computed } from 'vue'
import { useSetting } from '../../../../store/pinia';
import CheckboxInput from '@/components/custom/elements/CheckboxInput'
// import _ from 'lodash'

const store = useSetting();
const menuStyle = computed(() => store.sidebar_type_value)

</script>
