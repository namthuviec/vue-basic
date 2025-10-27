<template>
    <div>
        <h2>Submit form</h2>

        <form name="sampleForm">
            <div class="form-group">
                <label for="username">Username</label>
                <input name="username" type="text" placeholder="enter username" id="username" v-model="form.username" />
            </div>

            <div class="form-group">
                <label for="password">Password</label>
                <input name="password" type="password" placeholder="enter password" id="password"
                    v-model="form.passowrd" />
            </div>

            <button type="submit" @click="onSubmitForm">Submit</button>
        </form>
    </div>
</template>

<script>
export default {
    data() {
        return {
            form: {
                username: '',
                passowrd: ''
            }
        }
    },
    methods: {
        onSubmitForm(e) {
            e.preventDefault();
            console.log(this.form)
        }
    }
}
</script>

<style scoped>
form {
    padding: 100px;
    border: 1px solid #ccc;
}

.form-group {
    display: flex;
    flex-wrap: wrap;
}

label {
    display: inline-block;
    font-weight: 600;
    margin-bottom: 5px;
}

input {
    display: inline-block;
    padding: 10px;
    margin-bottom: 10px;
    background-color: #f9f9f9;
    width: 100%;
    border: 1px solid #ccc;
}

button {
    display: inline-block;
    padding: 10px;
    background-color: #f9f9f9;
    width: 100%;
    border: 1px solid #ccc;
}
</style>