<template>
    <div>
        <h1>Two way bindding</h1>
        <input name="username" type="text" placeholder="Enter username" v-model="username" />
        <p>UserName: {{ username }}</p>
        <p>Course: {{ course }}</p>
        <p>Time: {{ time }}</p>
        <p>Gender: {{ gender }}</p>
        <br />

        <!-- user select -->
        <select v-model="course">
            <option>--Chọn--</option>
            <option>php</option>
            <option>java</option>
            <option>csharp</option>
        </select>

        <br />

        <!-- User Checkbox -->
        <label for="Monday">Monday</label>
        <input type="checkbox" value="Monday" id="Monday" v-model="time" />

        <label for="Friday">Friday</label>
        <input type="checkbox" value="Friday" id="Monday" v-model="time" />

        <br />

        <!-- user radia -->
        <label for="male">Male</label>
        <input type="radio" value="male" id="male" v-model="gender" />

        <label for="female">Female</label>
        <input type="radio" value="Female" id="female" v-model="gender" />


    </div>
</template>

<script>
export default {
    data() {
console.log(this)

        return {
            username: '',
            course: 'java',
            time: ['Monday'],
            gender: 'male'
        }
    }
}

</script>