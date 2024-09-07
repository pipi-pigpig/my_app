<template>
    <div class="right">
        <div class="main">
            <h1>注册</h1>
            <p>输入您的电话号码以注册</p>
            <form>
                <div class="inputBox">
                    <select class="origin">
                        <option>+86</option>
                    </select>
                    <input type="tel" placeholder="请输入您的手机号" v-model="phoneNumber">
                </div>
                <div class="inputBox">
                    <input type="text" placeholder="请输入验证码">
                    <button class="code">获取验证码</button>
                </div>
                <div class="inputBox">
                    <div class="lock_icon"></div>
                    <input type="password" placeholder="请输入密码">
                </div>
                <div class="inputBox">
                    <div class="lock_icon"></div>
                    <input type="password" placeholder="请再次输入密码">
                </div>
                <div class="login">
                    <button>立即登录</button>
                </div>
            </form>

        </div>
    </div>
</template>

<script>
import { ref } from 'vue'
export default {
    name: 'resMode',
    setup() {
        const phoneNumber = ref('')
        return {
            phoneNumber
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
    background-color: rgb(255, 255, 255);
    display: flex;
    justify-content: center;
    align-items: center;
}

.right .main {
    width: 80%;
}


.right .main h1 {
    font-size: 2.7vw;
    margin-bottom: 0.5vw;
    font-family: fantasy;
}

.right .main p {
    /* 对应18px */
    font-size: 0.93vw;
    margin-bottom: 2.08vw;
    color: rgba(178, 186, 198, 1);
}

.right .main .inputBox {

    border: none;
    border-bottom: 1px solid #ccc;
    /* 这里定义了线条的颜色和粗细 */
    /* 24px */
    font-size: 1.25vw;
    padding: 0.26vw 0;
    outline: none;
    display: flex;
    flex-direction: row;
    margin: 1.04vw 0;
    color: rgba(178, 186, 198, 1);
}

.right .main .inputBox select {
    border: none;
    font-size: 0.93vw;
    padding: 0.26vw 0;
    outline: none;
    width: 12%;
}

.right .main .inputBox input {
    color: rgba(178, 186, 198, 1);
    width: 80%;
    border: none;
    font-size: 1.25vw;
    padding: 0.26vw 0;
    outline: none;
}

.right .main .inputBox .code {
    width: 30%;
    border: none;
    font-size: 1.25vw;
    padding: 0.26vw 0;
    outline: none;
    background: transparent;
    border-left: #ccc solid 1px;
    color: rgba(178, 186, 198, 1);
    cursor: pointer;
}

input::placeholder {
    color: rgba(178, 186, 198, 1);
    /* 默认情况下，placeholder可能会有透明度，这里设置为1确保颜色显示正常 */
}

.lock_icon {
    width: 2vw;
    background-image: url(../../assets/images/lock.png);
    background-size: cover;
    aspect-ratio: 0.83 / 1;
    margin-right: 2vw;
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