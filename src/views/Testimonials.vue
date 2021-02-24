<template>
    <div>
        <p>This is the Testimonial Page but we have no testimonials</p>
        <!-- <HelloWorld :msg="message" /> -->
        <HelloWorld @updateMessage="handleMessageUpdate" :msg="message" />

    </div>
</template>

<script>
import HelloWorld from '../components/HelloWorld.vue';

export default {
    name: "TestimonialPage",
    components: {
        HelloWorld
    },
    data() {
        return {
            message: "Welcome to Your Testimonial page"
        }
    },
    methods: {
        handleMessageUpdate(payload) {
            this.message = payload.msg;
        }
    },   
};
</script>

<style></style>