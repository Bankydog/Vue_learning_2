<template>
  <div>
    <FormComponent />
    <ListData :employees="employees" />
  </div>
</template>

<script>
import ListData from "./components/ListData.vue";
import FormComponent from "./components/FormComponent.vue";
export default {
  name: "App",
  components: {
    ListData,
    FormComponent,
  },
  data() {
    return {
      employees: [],
    };
  },
};
</script>

<style>
</style>