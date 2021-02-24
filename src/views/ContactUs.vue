<template>
    <div>        
        
        <form id="form">
            <h1 :title="message">{{ message }} {{firstName}} </h1>

            <label for="firstName"> First Name</label> <br> <br>
            <input v-model="firstName" type="text"/> <br> <br>

            <label for="email"> Email</label> <br> <br>
            <input v-model="email" type="email"/>

            <p>My name is: {{ firstName }}. I'm learning: {{ prog }}. My message is: <span class="messageText"> {{ messageText }} </span></p>

            <label for="firstName"> Choose program</label> <br> <br>
            <select v-model="prog" name="" id="">
                <option v-for="program in programs" :value="program" :key="program">
                    {{ program }}
                </option>
            </select> 
            <br> <br>
            
            <textarea v-model="messageText" name="" id="" cols="30" rows="10" type="text"></textarea>
            <br> <br>
            <button @click="submit">Submit</button>

        </form>
    </div>
</template>

<script>
    export default {
        name: "ContactUs",
        data() {
            return {
                message: "Welcome to Practice",
                firstName: "",
                email: "",
                programs: ["JavaScript", "HTML", "Vue", "jQuery"],
                prog: "",
                messageText: ""
            };
        },
        methods: {
            submit() {
                alert("Congratulations " +  this.firstName + "! Your message has been sent!")
            },
        },
    };
</script>

<style>
    .messageText {
        font-weight: bold;
    }
</style>