<template>
  <div>
    <FormComponent />
    <ListData :employees = "employees" />
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
      employees: [
        {
          name: "Bank",
          salary: 50000,
        },
        {
          name: "Bow",
          salary: 20000,
        },
        {
          name: "Belle",
          salary: 20000,
        },
        {
          name: "mergency",
        },
        {
          name: "Nam",
          salary: 500
          ,
        },
      ],
    };
  },
};
</script>

<style>
</style>