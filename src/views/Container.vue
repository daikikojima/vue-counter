<template>
  <div class="home">
    <h1>Count App (with props)</h1>
    <CountComponent :count="count" :update="update" />
  </div>
</template>

<script>
// @ is an alias to /src
import CountComponent from "@/components/CountComponent.vue";

export default {
  name: "container",
  components: {
    CountComponent
  },
  data() {
    return {
      count: 0
    };
  },
  methods: {
    update(cmd) {
      switch (cmd) {
        case "INCREMENT":
          this.count++;
          break;
        case "DECREMENT":
          this.count--;
          break;
        case "CLEAR":
          this.count = 0;
          break;
        default:
          break;
      }
    }
  }
};
</script>
<style scoped>
.home {
  padding: 10% 0;
}
</style>
