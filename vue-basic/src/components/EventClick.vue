<template>
    <div>
        <h1>Event click</h1>

        <p>{{ message }}</p>

        <button type="button" @click="showMessage">Show message</button>
        <button type="button" @click="showCourse('c#')">Show course</button>

    </div>
</template>

<script>
export default {
    data() {
        return {
            message: 'hhshsd'
        }
    },
    methods: {
        showMessage() {
            alert(this.message)
        },
        showCourse(course) {
            alert(course)
        }
    }
}
</script>