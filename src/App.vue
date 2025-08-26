<template>
  <div>
    <h1>Vue Exam Project</h1>

    <!-- Input to dynamically change username -->
    <input v-model="user" placeholder="Enter your name" />

    <!-- Greeting Component with Prop -->
    <Greeting :username="user" />

    <!-- Students Component -->
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
      user: "kyle" // default value
    };
  }
};
</script>
