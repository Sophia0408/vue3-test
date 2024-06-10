<template>
  <div :class="isCustom ? 'custom' : 'mine'"></div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
export default defineComponent({
  props: {
    isCustom: boolean,
  },
  setup() {
    return {};
  },
});
</script>
<style scoped lang="sass"></style>
