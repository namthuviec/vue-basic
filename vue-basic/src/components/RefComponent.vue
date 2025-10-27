<template>
    <div>
        <h2>Ref component</h2>

        <input type="text" ref="myInput" placeholder="enter some data" />

        <button @click="focusInput">Focus Input</button>

    </div>
</template>

<script>
import { ref } from 'vue';
export default {
    setup() {
        const myInput = ref(null);

        const focusInput = () => {
            console.log('myInput', myInput);
            myInput.value?.focus();
            myInput.value.value = 'sdasd'
            console.log('myInput:value', myInput.value?.value);
        }

        return {
            myInput,
            focusInput
        }
    }
}
</script>