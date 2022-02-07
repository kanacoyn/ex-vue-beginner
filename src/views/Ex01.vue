<template>
  <div class="sample">
    <p>名前:{{ name }}</p>
    <p>年齢:{{ age }}</p>
    <p>10年後の年齢:{{ age + 10 }}</p>
    趣味:
    <span v-for="hobby of hobbies" v-bind:key="hobby">{{ hobby }}&nbsp;</span>
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
import { Hobby } from "@/types/hobby";
@Component
export default class XXXComponent extends Vue {
  private name = "矢野佳夏子";
  private age = 25;
  private url = "https://www.nintendo.co.jp/hardware/switch/";
  private image = "/img/switch.jpg";
  private hobbies = ["水泳", "マラソン"];
}
</script>

<style scoped>
.sample {
  text-align: left;
  border: 3px solid black;
  width: 500px;
  padding: 5px;
}
</style>
