<template>
  <!-- template 에는 동일한 속성의 element가 병렬로 놓일수는 없음. -->

  <div>
    <!-- <app-header v-bind:프롭스 속성 이름="상위 컴포넌트 데이터 이름"></app-header> -->
    <app-header v-bind:propsdata="str" v-on:renew="renewStr"></app-header>
  </div>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";
// 기존에는 하나의 vue 파일에서 해결하려 하려던 사항을 전문적인 Part로 나누어 import 해서 사용하면 됨
// var AppHeader = {
//   template: "<header><h1>Header</h1></header>"
// };

export default {
  data: function() {
    return {
      str: "header"
    };
  },
  components: {
    "app-header": AppHeader
  },
  methods: {
    renewStr: function() {
      this.str = "You press renew Button";
    }
  }
};
</script>

<style>
</style>