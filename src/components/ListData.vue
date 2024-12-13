<template>
  <div>
    <PersonInfo name = "Bank" salary = 50000 />
    <PersonInfo name = "Bow" salary = 30000 />
    <PersonInfo name = "Belle" salary = 15000 />
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
      
    };
  },
};
</script>
  
<style scoped>

</style>