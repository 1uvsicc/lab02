<template>
  <div class="border border-gray-300 p-4 m-4 w-64 text-center mx-auto">
    <h3>{{ student.name }} {{ student.surname }}</h3>
    <p class="text-gray-500">GPA: {{ student.gpa }}</p>
  </div>
</template>

<script setup lang="ts">
import { defineProps } from 'vue'

const props = defineProps({
  student: {
    type: Object,
    required: true,
  },
})
</script>

<style scoped>
/*   .student-card {
    border: 1px solid #ccc;
    padding: 16px;
    margin: 10px;
    width: 200px;
    text-align: center;
  
  } */
</style>
