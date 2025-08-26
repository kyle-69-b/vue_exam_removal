<template>
  <div>
    <h1>Vue Exam Project</h1>

  
    <input v-model="user" placeholder="Enter your name" />

  >
    <Greeting :username="user" />

  
    <Students />
  </div>
</template>

<script>
import Greeting from "./components/Greeting.vue";
import Students from "./components/Students.vue";

export default {
  name: "App",
  components: { Greeting, Students },
  data() {
    return {
      user: "kyle" 
    };
  }
};
</script>
