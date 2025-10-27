<template>
    <div>
        <h2>Forloop</h2>

        <p v-for="item in courses" :key="item.index">

            <button type="button" @click="showCourse(item)">{{ item  }}</button>

        </p>

    </div>
</template>

<script>
export default {
    data() {
        return {
            courses: ['c#', 'java', 'php', 'python', ]
        }
    },
    methods: {
        showCourse(item) {
            alert(item)
        }
    }
}
</script>