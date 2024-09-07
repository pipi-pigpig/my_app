<template>
  <div class="outShell">
    <div class="light">
      <div class="container">
        <login-page v-if=isLogin></login-page>
        <res-page v-if=!isLogin></res-page>
      </div>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue'
import {provide} from 'vue'
import loginPage from './loginPage.vue'
import resPage from './resPage.vue'
export default {
    name:'IndexPage',
    components: {
      loginPage,
      resPage
    },
    setup() {
      const isLogin = ref(false)
      provide('isLogin',isLogin)
      return {
        isLogin
    }
  }
}
</script>

<style scoped>
.outShell {
  width: 100vw;
  height: 100vh;
  background-image: url(../assets/images/back.png);
  background-size: cover;
  background-repeat: no-repeat;
  display: flex;
}

.light {
  width: 100%;
  height: 100%;
  background-color: rgba(255, 255, 255, 0.6);
  display: flex;
  justify-content: center;
  align-items: center;
}

.container {
  width: 75vw;
  /* background-color: red; */
  /* 可能出现不兼容问题 */
  aspect-ratio: 1.85 / 1;
  display: flex;
  flex-direction: row;
}



</style>