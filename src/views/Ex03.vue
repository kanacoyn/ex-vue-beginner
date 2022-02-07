<template>
  <div class="ex3">
    <input type="text" v-model.number="num1" />
    +
    <input type="text" v-model.number="num2" />
    =
    {{ num1 + num2 }}
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
@Component
export default class XXXComponent extends Vue {
  private num1 = "";
  private num2 = "";
}
</script>

<style scoped></style>
