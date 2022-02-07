<template>
  <div class="sample">
    <p>名前:{{ name }}</p>
    <p>年齢:{{ age }}</p>
    <p>10年後の年齢:{{ age + 10 }}</p>
    <p>趣味:{{ hobby }}</p>
    <p>
      <a v-bind:href="url">会社リンク</a>
    </p>
    <div class="info">
      <img v-bind:src="image" />
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
@Component
export default class XXXComponent extends Vue {
  private name = "矢野佳夏子";
  private age = 25;
  private hobby = ["スイム", "バイク"];
  private url = "https://www.nintendo.co.jp/hardware/switch/";
  private image = "../img/switch.jpg";
}
</script>

<style scoped>
.sample {
  text-align: left;
  border: 3px solid black;
  padding: 5px;
}

.info {
  border: 2px solid;
  padding: 5px;
}
</style>
