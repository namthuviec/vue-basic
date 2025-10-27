<template>
    <div class="button">
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

<style>

.button {
    padding: 10px;
    border: 1px solid #ccc;
    background-color: #f9f9f9;
    margin-bottom: 10px;
    width: 100px;
    text-align: center;
    cursor: pointer;
}

</style>