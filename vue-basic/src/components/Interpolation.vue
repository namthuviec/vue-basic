<template>
    <div>
        <h1>Interpolation & data</h1>
        <h2>{{ message }}</h2>
        <h2>{{ number + 5 }}</h2>
        <h2>{{ sayHello() }}</h2>
    </div>
</template>

<script>
export default {
    data() {
        return {
            message: 'Xin chào vuejs3',
            number: 5
        }
    },
    methods: {
        sayHello () {
            return "Xin chào bạn"
        }
    },
}
</script>