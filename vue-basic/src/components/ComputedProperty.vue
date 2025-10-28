<template>
    <div>
        <h2>Computed Vue</h2>
        <p>Original Message: {{ originalMessage }}</p>
        <p>Reversed Message: {{ reservedMessage }}</p>
        <input type="text" name="message" v-model="originalMessage" placeholder="enter orginal message" />
        <p>Counter: {{ counter }}</p>

        <button @click="incrementCounter">+</button> 
        &nbsp;
        <button @click="decrementCounter">-</button>
    </div>
</template>

<script>
import { ref, computed } from 'vue';

export default {
    setup() {
        const originalMessage = ref('');
        const counter = ref(0);

        const reservedMessage = computed(() => {
            console.log('Message data: ', originalMessage);
            return originalMessage.value.split('').reverse().join('')
        })

        const incrementCounter = () => {
            counter.value ++;
        }

        const decrementCounter = () => {
            counter.value --;
        }

        return { originalMessage, reservedMessage, counter, incrementCounter, decrementCounter }
    }
}
</script>

<style>
button {
    padding: 10px;
    width: 50px;
    height: 50px;
}
</style>