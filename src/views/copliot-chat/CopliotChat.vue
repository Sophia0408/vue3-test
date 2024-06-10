<template>
  <div class="wrap">
    <div class="header">header</div>
    <div class="main"></div>
    <div class="footer">footer</div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
export default defineComponent({
  name: "CopliotChat",
  setup() {
    return {};
  },
});
</script>
<style scoped>
html,
body {
  height: 100%;
}
.wrap {
  display: -webkit-box;
  display: -webkit-flex;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-orient: vertical;
  -webkit-flex-direction: column;
  -ms-flex-direction: column;
  flex-direction: column;
  width: 100%;
  height: 100%;
}
.header,
.footer {
  height: 40px;
  line-height: 40px;
  background-color: #d8d8d8;
  text-align: center;
}
.main {
  -webkit-box-flex: 1;
  -webkit-flex: 1;
  -ms-flex: 1;
  flex: 1;
  width: 100%;
  overflow: auto; /* winphone8和android4+ */
  -webkit-overflow-scrolling: touch; /* ios5+ */
}
</style>
