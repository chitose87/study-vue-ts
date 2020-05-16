<template lang="pug">
  main
    .continer
      h2 スライダーを作ってみる
      h3 正解例
      .slider
        .slider__body(v-bind:style="`transform: translateX(${percent}%);`")
          .slider__item(v-for="img in imgList")
            img(v-bind:src="img" alt="")

        .slider__ui
          button.slider__prev(v-on:click="onPrev()")
            | 前へ
          span.slider__num
            span.slider__current(v-html="currentValue")
            |/
            span.slider__total(v-html="imgList.length")
          button.slider__next(v-on:click="onNext()")
            | 次へ

</template>

<script lang="ts">
// ここからTypescript
import { Component } from "~/node_modules/vue-property-decorator";
import { Vue } from "~/node_modules/nuxt-property-decorator";

@Component({
  components: {}
})
export default class HogePage extends Vue {
  // 変数の宣言
  imgList = [
    "https://placehold.jp/ff0000/ffffff/600x400.png?text=A",
    "https://placehold.jp/ff0000/ffffff/600x400.png?text=B",
    "https://placehold.jp/ff0000/ffffff/600x400.png?text=C",
    "https://placehold.jp/ff0000/ffffff/600x400.png?text=D",
    "https://placehold.jp/ff0000/ffffff/600x400.png?text=E",
    "https://placehold.jp/ff0000/ffffff/600x400.png?text=D",
    "https://placehold.jp/ff0000/ffffff/600x400.png?text=F",
    "https://placehold.jp/ff0000/ffffff/600x400.png?text=G"
  ];

  percent = 0;
  currentValue = 1;

  // 関数たち
  mounted() {
    console.log("mounted", "初期化されたよ");
  }

  /**
   * template の v-on:click="onPrev()"
   */
  onPrev() {
    console.log("onPrev");
    if (this.currentValue > 1) {
      this.currentValue -= 1;
      this.percent = this.getPercentValue(this.currentValue);
    }
  }
  /**
   * template の v-on:click="onNext()"
   */
  onNext() {
    console.log("onNext");
    if (this.currentValue < this.imgList.length) {
      this.currentValue += 1;
      this.percent = this.getPercentValue(this.currentValue);
    }
  }

  /**
   * ％の計算をする
   */
  private getPercentValue(current: number) {
    let a = (current - 1) * -100;
    console.log("getPercentValue", a);
    return a;
  }
}
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  &,
  &::before,
  &::after {
    box-sizing: border-box;
  }
}
main {
  background-color: whitesmoke;
}
.continer {
  width: 100%;
  max-width: 900px;
  margin-left: auto;
  margin-right: auto;
  padding: 1.5rem;
  background-color: white;
  position: relative;
}
// ここまでベーススタイル

// スライダーのスタイル
.slider {
  width: 100%;
  //overflow（はみ出た）分は見えなくする
  overflow-x: hidden;
  &__body {
    width: 100%;
    white-space: nowrap; //改行しないように
    // アニメーションはここで設定している
    transition: transform 0.6s ease-in-out 0s;
  }
  &__item {
    width: 100%;
    display: inline-block; //インライン要素に変更
    border: 2px solid gray;
    padding: 1rem;
    img {
      display: block;
      width: 100%;
      height: auto;
    }
  }
  &__prev {
  }
  &__next {
  }
}
</style>
