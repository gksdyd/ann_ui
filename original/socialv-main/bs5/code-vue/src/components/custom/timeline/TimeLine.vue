<template>
  <ul class="iq-timeline ms-1">
    <li v-for="(item, index) in items" :key="index">
      <div class="timeline-dots" :class="'border-' + item.color"></div>
      <div class="d-flex align-items-center justify-content-between">
        <h6 class="mb-1" v-html="item.title"></h6>
        <small v-html="item.right"></small>
      </div>
      <div class="d-inline-block w-100">
        <p v-html="item.description"></p>
        <template
          v-if="item.child.items.length > 0 && item.child.type === 'img'"
        >
          <div class="media-group">
            <a href="#" class="iq-media">
              <img
                src="@/assets/images/user/01.jpg"
                class="img-fluid avatar-40 rounded-circle"
                alt="img"
              />
            </a>
            {{ "" }}
            <a href="#" class="iq-media">
              <img
                src="@/assets/images/user/02.jpg"
                class="img-fluid avatar-40 rounded-circle"
                alt="img"
              />
            </a>
            {{ "" }}
            <a href="#" class="iq-media">
              <img
                src="@/assets/images/user/03.jpg"
                class="img-fluid avatar-40 rounded-circle"
                alt="img"
              />
            </a>
            {{ "" }}
            <a href="#" class="iq-media">
              <img
                src="@/assets/images/user/07.jpg"
                class="img-fluid avatar-40 rounded-circle"
                alt="img"
              />
            </a>
            {{ "" }}
            <a href="#" class="iq-media">
              <img
                src="@/assets/images/user/05.jpg"
                class="img-fluid avatar-40 rounded-circle"
                alt="img"
              />
            </a>
            {{ "" }}
            <a href="#" class="iq-media">
              <img
                src="@/assets/images/user/06.jpg"
                class="img-fluid avatar-40 rounded-circle"
                alt="img"
              />
            </a>
          </div>
        </template>
      </div>
    </li>
  </ul>
</template>

<script>
export default {
  name: "TimeLine",
  props: {
    items: { type: Array, default: () => [] },
  },
};
</script>
