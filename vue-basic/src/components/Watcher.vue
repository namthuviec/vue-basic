<template>
    <div>
        <h2>Watcher</h2>

        <p>Current message: {{  message }}</p>
        <input type="text" v-model="message" placeholder="enter message" />

    </div>
</template>

<script>
import { ref, watch, watchEffect } from 'vue'
export default {
    setup() {
        const message = ref('')

        watch(message, (newValue, oldValue) => {
            console.log(`message changed from ${oldValue} to ${newValue}`)
        }, { immediate: true, deep: true })

        watchEffect(() => {
            console.log('message changed: ', message.value)
        })

        return { message }
    }
}
</script>