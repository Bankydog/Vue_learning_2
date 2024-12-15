<template>
  <div>
    <h1>Employee's Data</h1>
    <FormComponent @save="insertEmployee" />
    <section class="employee-content" v-if="employees.length > 0">
      <ListData
        :employees="employees"
        @update-visibility="updateEmployeeVisibility"
        @delete-employee="deleteEmployee"
      />
    </section>
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
  methods: {
    insertEmployee(data) {
      const newEmployee = {
        ...data,
        id: this.employees.length > 0 ? this.employees[this.employees.length - 1].id + 1 : 1,
        isVisible: false,
      };
      this.employees.push(newEmployee);
    },
    updateEmployeeVisibility(id) {
      this.employees = this.employees.map((item) =>
        item.id === id ? { ...item, isVisible: !item.isVisible } : item
      );
    },
    deleteEmployee(id) {
      this.employees = this.employees.filter((item) => item.id !== id);
    },
  },
};
</script>

<style>
* {
  box-sizing: 0px;
  padding: 0px;
  margin: 0px;
}
</style>
<style scoped>
div {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  padding: 8px;
  background: rgb(24, 24, 24);
  color: white;
}

</style>
