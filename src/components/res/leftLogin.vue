<template>

    <div class="left">
        <div class="login">
            <button @click=login>登录</button>
        </div>
    </div>
</template>

<script>
import { inject } from 'vue'

export default {
    name: 'leftLogin',
    setup(){
        const isLogin = inject('isLogin')
        function login(){
            console.log(isLogin)
            isLogin.value = true
        }
    return {
        isLogin,
        login
    }
}
}
</script>

<style>
.left{
    width: 50%;
    height: 100%;
}
.login {
    margin-top: 2.08vw;
    width: 100%;
    display: flex;
    justify-content: center;
}

.login button {

    padding: 0.54vw 0;
    border: none;
    border-radius: 0.624vw;
    background: linear-gradient(to right, rgba(255, 202, 171, 1), rgba(95, 173, 127, 1));
    color: white;
    font-size: 1.6vw;
    font-weight: 500;
    cursor: pointer;
    width: 22.6vw;
    aspect-ratio: 8 /1;
}

.left {
    background-color: rgba(255, 255, 255, 0.437);
    display: flex;
    justify-content: center;
    align-items: center;
}
</style>