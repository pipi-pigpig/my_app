<template>
    <left-login></left-login>
    <res-mode></res-mode>  
</template>

<script>
import resMode from './res/resMode.vue'
import leftLogin from './res/leftLogin.vue'
export default {
    name: 'resPage',
    components:{
        resMode,
        leftLogin
    }
}
</script>

<style scoped>

</style>