<template>
  <div>Job page for job {{ currentJobId }}</div>
</template>

<script>
export default {
  name: "JobView",
  computed: {
    currentJobId() {
      console.log(this.$route);
      return 5;
    },
  },
};
</script>

<style></style>
