<template>
  <div class="message-input">
    <slot></slot>
    <div class="input">
      <input v-model="message" type="text" placeholder="输入消息..." />
      <div class="more">
        <img class="addEmoji" @click="emojiClick" />
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
export default defineComponent({
  setup() {
    return {};
  },
});
</script>
<style scoped lang="less"></style>
