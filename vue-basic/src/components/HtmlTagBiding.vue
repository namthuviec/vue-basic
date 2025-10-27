<template>
    <div>
        <h1 v-html="htmlContent"></h1>
        <h2 v-html="dynamicContent"></h2>
        <button @click="loadHtml">Load Html</button>
    </div>
</template>

<script>
export default {
    data() {
        return {
            htmlContent: '<strong>Hello vuejs 2</strong>',
            dynamicContent: ''
        }
    },
    methods: {
        loadHtml() {
            this.dynamicContent = '<strong>dynamic html content</strong>' + new Date().toISOString() 
        }
    }
}
</script>