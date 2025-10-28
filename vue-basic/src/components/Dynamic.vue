<template>
    <div>
        <h2>Dynamic Component</h2>
        <button @click="currentComponent = 'ComponentA'">Show Component A</button>
        <button @click="currentComponent = 'ComponentB'">Show Component B</button>

        <component :is="currentComponent" />
    </div>
</template>

<script>
import ComponentA from './ComponentA.vue';
import ComponentB from './ComponentB.vue';

export default {
    components: {
        ComponentA,
        ComponentB
    },
    data() {
        return {
            currentComponent: ComponentA
        }
    }
}
</script>