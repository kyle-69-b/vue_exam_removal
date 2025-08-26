<template>
  <div>
    <h2>Student List</h2>

   
    <ul v-if="showList">
  
      <li v-for="(student, index) in studentScores" :key="index"
          :class="{ highlight: student.score >= 90 }">
        {{ student.name }} - {{ student.score }}
      </li>
    </ul>

  
    <p>Passing Students: {{ passingCount }}</p>
  </div>
</template>

<script>
export default {
  name: "Students",
  data() {
    return {
      showList: true,
      studentScores: [
        { name: "kyle", score: 95 },
        { name: "kyle2", score: 65 },
        { name: "kyle3", score: 75 },
        { name: "kyle4", score: 90 }
      ]
    };
  },
  computed: {
    passingCount() {
      return this.studentScores.filter(s => s.score >= 70).length;
    }
  }
};
</script>

<style>
.highlight {
  color: green;
  font-weight: bold;
}
</style>
