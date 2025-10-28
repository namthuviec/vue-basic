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

            <button type="button" @click="onSubmitForm">Submit</button>

            <p style="color: red;" v-for="error in errors" :key="error.index">
                {{ error }} is required!
            </p>
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
            },
            errors: []
        }
    },
    methods: {
        onSubmitForm() {
            this.errors = [];
            for (const item in this.form) {
                if (this.form[item] === '' || this.form[item].length === 0) {
                    this.errors.push(item);
                }
            }
            if (this.errors.length === 0) {
                console.log('submit', this.form, JSON.parse(JSON.stringify(this.form)))

            } else {
                for (const index in this.errors) {
                    console.log(this.errors[index] + ' is required!')
                }
            }
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