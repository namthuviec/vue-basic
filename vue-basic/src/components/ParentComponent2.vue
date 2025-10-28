<template>
    <div>
        <h2>Lifecycle Hooks example</h2>
        <button @click="showChild = !showChild">Toogle Child Component</button>

        <ChildComponent2 v-if="showChild"></ChildComponent2>
    </div>
</template>

<script>
import ChildComponent2 from './ChildComponent2.vue';

export default {
    data() {
        return {
            showChild: false
        }
    },
    components: {
        ChildComponent2
    }
}
</script>,