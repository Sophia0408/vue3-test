<template>
  <div class="message-item">
    <p v-if="type === 'other'" class="avatar">
      <img v-lazy="IMG_URL + custom.avatar" alt="" />
    </p>
    <div></div>
    <p v-if="type === 'mine'" class="avatar">
      <img v-lazy="IMG_URL + userInfo.avatar" alt="" />
    </p>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
export default defineComponent({
  props: {
    type: String,
    custom: Object,
  },
  setup() {
    return {};
  },
});
</script>
<style scoped lang="less"></style>
