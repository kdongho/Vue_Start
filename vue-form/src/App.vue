<template>
  <form v-on:submit.prevent="submitForm">
    <!-- 아래 button에서 submit이 발생할 경우, 이벤트 버블을 통해 하위에서 발생한 이벤트가 상위 Layer에 영향을 미치고, 이를 통해 특정 method가 실행 되도록 처리하면 됨. -->
    <div>
      <label for="username">id: </label>
      <input id="username" type="text" v-model="username" />
    </div>
    <div>
      <label for="password">pw: </label>
      <input id="password" type="password" v-model="password" />
    </div>
    <button type="submit">login</button>
  </form>
</template>

<script>
import axios from "axios";
// npm i axios 를 이용하여, axios module을 설치한 이후, global 선언된 axios로부터 axios를 가져올 수 있다!

export default {
  data: function() {
    return {
      username: "",
      password: ""
    };
  },
  methods: {
    submitForm: function() {
      // event.preventDefault();
      // event가 발생해도 새로고침을 막아주기 위해, 삽입하는 문구
      // 하지만 vue.js에서는 event가 발생하는 근원(v-on.submit에 prevent 추가 옵션을 붙여 해결할 수 있다.)
      console.log(this.username, this.password);
      var url = "https://jsonplaceholder.typicode.com/users/";
      var data = {
        username: this.username,
        password: this.password
      };
      axios
        .post(url, data)
        //axios의 목적인 특정 서버와 통신하기 위한 방법입니다!
        .then(function(response) {
          console.log(response);
        })
        .catch(function(error) {
          console.log(error);
        });
    }
  }
};
</script>

<style></style>
