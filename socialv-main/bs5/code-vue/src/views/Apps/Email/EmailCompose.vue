<template>
  <div class="content-inner" id="page_layout">
    <b-container>
      <ComposeBody />
    </b-container>
  </div>
</template>

<script>
import ComposeBody from "./ComposeBody";
// import { socialvue } from '../../../config/pluginInit'
export default {
  name: "EmailCompose",
  components: { ComposeBody },
};
</script>
