<template>
  <h2>Hello, {{ formattedUsername }}</h2>
</template>

<script>
import { capitalize } from "../utils";

export default {
  name: "Greeting",
  props: {
    username: {
      type: String,
      required: true
    }
  },
  computed: {
    formattedUsername() {
      return capitalize(this.username);
    }
  }
};
</script>
