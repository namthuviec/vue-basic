<template>
    <div>
        <h3>Component Child</h3>
        <p>{{ message }}</p>
    </div>
</template>

<script>
export default {
    props: {
        message: String
    }
}
</script>