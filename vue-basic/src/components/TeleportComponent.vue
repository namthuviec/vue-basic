<template>
    <div>
        <h1>Use sample teleport</h1>
        <button @click="showModal = true">Show modal</button>

        <Teleport to="body">
            <div v-if="showModal" class="modal">
                <div class="modal-content">
                    <h2>Modal title</h2>
                    <p>content....................</p>
                    <p>content....................</p>
                    <p>content....................</p>
                    <p>content....................</p>
                    <button @click="showModal = false">Close</button>
                </div>
            </div>
        </Teleport>
    </div>
</template>

<script>

export default {
    data() {
        return {
            showModal: false
        }
    }
}
</script>

<style>
.modal {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    min-width: 500px;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: rgba(0, 0, 0, 0.5);
}

.modal-content {
    background-color: #fff;
    padding: 20px;
    border-radius: 4px;
}
</style>