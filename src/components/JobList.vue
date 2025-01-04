<script setup>
import jobData from "@/jobs.json";
import { ref } from "vue";

const jobs = ref(jobData);
console.log(jobs.value);
</script>

<template>
  <h2>Job List</h2>
</template>
