//var appHeader = {
//  template: "<div>Header</div>",
//  methods: {
//    addNumber: function() {
//      this.num += 1;
//   }
//  }
//};

// vue 파일은 아래와 같이 구성됩니다.
// template / script / style
// 각각의 파트는 실제 출력될 template part
// js 를 수행할 script 파트
// css를 수행할 style로 나뉘어 집니다.

<template>
  <!-- HMTL -->
  <div>Header</div>
</template>

<script>
export default {
  // javascript - 인스턴스 옵션
  methods: {
    addNumber: function() {
      this.num += 1;
    }
  }
};
</script>

<style>
/* css */
</style>