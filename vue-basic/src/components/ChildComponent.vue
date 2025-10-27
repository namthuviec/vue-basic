<template>
    <div>
        <input type="text" placeholder="enter some text" v-model="childData" />
        <button @click="sendData">Send data to parent</button>
    </div>
</template>

<script>
export default {
    data() {
        return {
            childData: ''
        }
    },
    methods: {
        sendData() {
            this.$emit('updateDataParent', this.childData)
        }
    }
}
</script>