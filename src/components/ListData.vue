<template>
  <div>
    <ul>
      <Person-info
        v-for="(item, index) in employees"
        :key="index"
        :name="item.name"
        :salary="item.salary"
      />
    </ul>
  </div>
</template>
  
  <script>
import PersonInfo from "./PersonInfo.vue";
export default {
  name: "ListData",
  components: {
    PersonInfo,
  },
  props: ["employees"],
  data() {
    return {};
  },
};
</script>
  
<style scoped>
</style>