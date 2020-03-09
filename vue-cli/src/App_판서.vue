<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <!-- <hello-world></hello-world>// 캐바피크 기법, VScode 의 바로가기 function 및 vue js 스타일 가이드상 공식 추천방식
    <HelloWorld></HelloWorld>// 파스칼 케이스
    <HelloWorld />//파스칼 케이스 advanced 닫는 부분이 없음-->
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  // 인스턴스 옵션 속성 or 컴포넌트 옵션 속성을 작성한다.
  name: "App",
  components: {
    HelloWorld
    // = 'hello-world': Helloworld
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
