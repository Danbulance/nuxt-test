<script setup lang="ts">
const { data, status, error, refresh, clear } = await useFetch(
  "https://bytegrad.com/course-assets/projects/corpcomment/api/feedbacks"
);
</script>

<template>
  <div>
    <h1>About Page</h1>
    <p>This is the about page.</p>

    <!-- Show data only if it's available -->
    <div v-if="data">
      <h2>Feedback Data</h2>
      <ul>
        <!-- Loop through the entire data object -->
        <li v-for="(item, index) in data" :key="index">
          {{ item }}
        </li>
      </ul>
    </div>

    <!-- Handle loading and errors -->
    <p v-if="!data && !error">Loading...</p>
    <p v-if="error">Error: {{ error.message }}</p>
  </div>
</template>
