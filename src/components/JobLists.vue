<script setup>
import data from "@/jobs.json";
import { ref } from "vue";
import JobList from "@/components/JobList.vue";

const jobLists = ref(data["jobs"]);
// console.log(jobLists.value);
</script>

<template>
  <section class="bg-green-50 px-4 py-10">
    <div class="container-xl lg:container m-auto">
      <h2 class="text-3xl font-bold text-green-500 mb-6 text-center">
        Browse Jobs
      </h2>
      <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
        <JobList v-for="job in jobLists" :key="job.id" :job="job"></JobList>
      </div>
      <section class="m-auto max-w-lg my-10 px-6">
        <a
          href="jobs.html"
          class="block bg-black text-white text-center py-4 px-6 rounded-xl hover:bg-gray-700"
          >View All Jobs</a
        >
      </section>
    </div>
  </section>
</template>
