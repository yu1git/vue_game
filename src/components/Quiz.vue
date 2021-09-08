<template>
  <div class="alert alert-info">
    <h2>{{ title }}</h2>
    <p>{{ quiz }}</p>
  </div>
</template>

<script>
export default {
  name: "Quiz",
  props: {
    title: String,
    quiz:String,
  }
  
};
</script>
