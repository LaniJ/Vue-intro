<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue';

export default {
  name: 'Home',
  data() {
    return {
      key: 0
    };
  },
  mounted() {
    setTimeout(() => {
      this.key += 1
    }, 5000);
  },
  components: {
    HelloWorld
  },
};
</script>
