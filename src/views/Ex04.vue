<template>
  <div class="sample">
    <input type="text" v-model.number="item1" /><br />
    <input type="text" v-model.number="item2" /><br />
    <input type="text" v-model.number="item3" /><br />

    税抜き価格:{{ item1 + item2 + item3 }}円<br />
    税込価格:{{ (item1 + item2 + item3) * 1.1 }}円
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
@Component
export default class XXXComponent extends Vue {
  private item1 = 0;
  private item2 = 0;
  private item3 = 0;
}
</script>

<style scoped></style>
