<template>
    <div class="left">
        <div class="main">
            <h1>登录</h1>
            <p>输入您的电话号码以登录</p>
            <form>
                <div class="inputBox">
                    <select class="origin">
                        <option>+86</option>
                    </select>
                    <input type="tel" placeholder="请输入您的手机号">
                </div>
                <div class="inputBox">
                    <div class="lock_icon"></div>
                    <input type="password" placeholder="请输入密码">
                    <a href="#">忘记密码？</a>
                </div>
                <div class="login">
                    <button>立即登录</button>
                </div>
            </form>
            <div class="bottom">
                <div class="text">
                    其他方式登录
                </div>
                <div class="apps">
                    <div class="qq"></div>
                    <div class="wechat"></div>
                    <div class="sina"></div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name:'loginMode',
}
</script>

<style scoped>
.left{
    width: 50%;
    height: 100%;
}

.left {
    background-color: rgb(255, 255, 255);
    display: flex;
    justify-content: center;
    align-items: center;
}

.left .main {
    width: 80%;
}


.left .main h1 {
    font-size: 2.7vw;
    margin-bottom: 0.5vw;
    font-family: fantasy;
}

.left .main p {
    /* 对应18px */
    font-size: 0.93vw;
    margin-bottom: 2.08vw;
    color: rgba(178, 186, 198, 1);
}

.left .main .inputBox {

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

.left .main .inputBox select {
    border: none;
    font-size: 0.93vw;
    padding: 0.26vw 0;
    outline: none;
    width: 12%;
}

.left .main .inputBox input {
    color: rgba(178, 186, 198, 1);
    width: 80%;
    border: none;
    font-size: 1.25vw;
    padding: 0.26vw 0;
    outline: none;
}

input::placeholder {
    color: rgba(178, 186, 198, 1);
    /* 默认情况下，placeholder可能会有透明度，这里设置为1确保颜色显示正常 */
}

.left .main .inputBox a {
    display: flex;
    width: 5.5vw;
    font-size: 0.93vw;
    color: rgba(178, 186, 198, 1);
    text-decoration: none;
    align-items: center;


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

.bottom {
    margin-bottom: 2.08vw;
}

.text {
    margin-top: 2.08vw;
    font-size: 0.93vw;
    color: rgba(178, 186, 198, 1);
    margin-bottom: 20px;
    text-align: center;
}

.apps {
    display: flex;
    margin-top: 1.04vw;
    flex-direction: row;
    justify-content: center;
    padding: auto;
}

.apps div {
    margin: auto;
    width: 7.4vw;
    aspect-ratio: 3.51 /1;
}

.qq {
    background-image: url(../../assets/images/QQ.png);
    background-size: cover;
}

.wechat {
    background-image: url(../../assets/images/wechat.png);
    background-size: cover;

}

.sina {
    background-image: url(../../assets/images/sina.png);
    background-size: cover;
}
</style>