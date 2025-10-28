<template>
    <Slots>
        <template #header>
            <div>Header</div>
        </template>
        <template #default>
            <div>LayoutWithSlots</div>
        </template>
        <template #footer>
            <div>Footer</div>
        </template>
    </Slots>
</template>

<script setup>
import Slots from './Slots.vue';
</script>