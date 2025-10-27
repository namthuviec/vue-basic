<template>
    <div>
        <h2>Sample condition if</h2>

        <button type="button" @click="onLogin">{{ isLogin ? 'Logout' : 'login'}} </button>

        <p v-if="isLogin">Welcome to user!</p>
        <p v-else>Please login!</p>
        
    </div>
</template>

<script>
export default {
    data() {
        return {
            isLogin: true
        }
    },
    methods: {
        onLogin() {
            this.isLogin = !this.isLogin;
        }
    }
}
</script>

