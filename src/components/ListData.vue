<template>
  <div>
    <h1>{{ message }}</h1>
    <PersonInfo />
    <PersonInfo />
    <PersonInfo />
    <PersonInfo />
  </div>
</template>
  
  <script>
import PersonInfo from "./PersonInfo.vue";
export default {
  name: "ListData",
  components: {
    PersonInfo,
  },
  data() {
    return {
      message: "List name of employee",
    };
  },
};
</script>
  
<style scoped>
h1 {
  color: green;
}
</style>