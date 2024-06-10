<template>
  <div ref="messageList" class="message-list">
    <ul ref="msglist" class="chat-message">
      <li
        v-for="(v, i) in chatList"
        :key="i"
        :class="[{ org: v.type === 'org' }]"
      >
        <template v-if="v.type === 'other'">
          <message-item type="other" :v="v" class="other" />
        </template>
        <template v-if="v.type === 'mine'">
          <message-item type="mine" :v="v" class="mine" />
        </template>
        <template v-if="v.type === 'org' && v.roomId.split('-').length > 1">
          <span>现在可以开始聊天了</span>
        </template>
        <template v-if="v.type === 'org' && v.roomId.split('-').length == 1">
          <span>
            系统消息：<span class="org-hightlight">{{ v.nickname }}</span
            >加入群聊！</span
          >
        </template>
      </li>
    </ul>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import messageItem from "../message-item/messageItem.vue";
export default defineComponent({
  name: "MesList",
  components: { messageItem },
  props: ["chatList"],
  setup() {
    return {};
  },
});
</script>
<style scoped lang="less"></style>
