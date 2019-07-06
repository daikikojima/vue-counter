<template>
  <div class="home">
    <h1>Count App</h1>
    <Count />
  </div>
</template>

<script>
// @ is an alias to /src
import Count from "@/components/Count.vue";

export default {
  name: "home",
  components: {
    Count
  }
};
</script>
<style scoped>
.home {
  padding: 10% 0;
}
</style>
