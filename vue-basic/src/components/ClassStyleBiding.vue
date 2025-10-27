<template>
    <div>
        <h2 :class="{active: isActive, inactive: !isActive}">Class style binding</h2>
        <p :style="styleObject">Hello, i am lon</p>
    </div>
</template>

<script>
export default {
    data() {
        return {
            isActive: false,
            styleObject: {
                color: 'purple',
                fontSize: '18px'
            }
        }
    }
}
</script>

<style>

.active {
    color: red;
}

.inactive {
    color: green;
}

</style>