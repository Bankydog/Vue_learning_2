<template>
  <div>
    <p>
      {{ name }} {{ salary }}
    </p>
  </div>
</template>

<script>
export default {
  name: "PersonInfo",
  data() {
    return {
      message: "employee information",
    };
  },
  props: ["name", "salary"]
};
</script>

<style scoped>

</style>