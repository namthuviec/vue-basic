<template>
    <div>
        <h2>Data From Child Component: {{ parentData }}</h2>
        <ChildComponent @updateDataParent="handleUpdateData" />
    </div>
</template>

<script>
import ChildComponent from './ChildComponent.vue';
export default {
    data() {
        return {
            parentData: ''
        }
    },
    components: {
        ChildComponent
    },
    methods: {
        handleUpdateData(dataChild) {
            console.log(dataChild);
            this.parentData = dataChild;
        }
    }
}
</script>,