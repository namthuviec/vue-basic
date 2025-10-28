<template>
    <div>
        <h2>This is Child component</h2>
        <p>Message: {{ message }}</p>
    </div>
</template>

<script>
export default {
    data() {
        return {
            message: 'Hello vuejs3'
        }
    },
    beforeCreate() {
        console.log('Thực hiện các mã code cần chạy trước khi component được tạo')
    },
    created() {
        console.log('THực hiện các mã code sau khi componnent đã tạo');
        this.message = 'created'
    },
}
</script>