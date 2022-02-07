<template>
  <div class="sample">
    <p>名前: {{ name }}</p>
    <p>年齢:{{ age }}歳</p>
    <p>10年後の年齢:{{ tenAge }}歳</p>
    <p>趣味:{{ hobby }}</p>
    <br />
    <a v-bind:href="url">会社リンク</a>
    <br />
    <img v-bind:src="image" />
    <hr />

    <button type="button" v-bind:disabled="falseflag" v-on:click="pressButton">
      ボタン
    </button>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
@Component
export default class XXXComponent extends Vue {
  private name = "";
  private age = 0;
  private tenAge = 0;
  private hobby = "";
  private url = "";
  private image = "";
  private falseflag = false;

  pressButton(): void {
    this.name = "矢野佳夏子";
    this.age = 25;
    this.tenAge = this.age + 10;
    this.hobby = "スイム,マラソン";
    this.url = "https://www.nintendo.co.jp/hardware/switch/";
    this.image = "../img/switch.jpg";

    if (this.falseflag) {
      this.falseflag = false;
    } else {
      this.falseflag = true;
    }
  }
}
</script>

<style scoped>
.sample {
  text-align: left;
  border: 4px solid black;
  width: 600px;
  padding: 10px;
}
</style>
