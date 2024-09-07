<template>
    <div class="right">
        <div class="res">
            <button @click="res">注册</button>
        </div>
    </div>
</template>

<script>
import { inject } from 'vue'
export default {
    name:'rightRes',
    setup() {
        const isLogin = inject('isLogin')
        function res() {
            console.log(isLogin)
            isLogin.value = false
        }
        return {
            res
    }
}
}
</script>

<style scoped>
.right {
    width: 50%;
    height: 100%;
}
.right {
    background-color: rgba(255, 255, 255, 0.437);
    display: flex;
    justify-content: center;
    align-items: center;
}

.res {
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
}

.res button {

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
</style>