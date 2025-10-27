<template>
    <div>
        <h2>Component Parent</h2>

        <Child :message="message"></Child>
    </div>
</template>

<script>
import Child from '@/components/Child.vue';
export default {
    components: {
        Child
    },
    data() {
        return {
            message: 'Hello from component parent'
        }
    }
}
</script>