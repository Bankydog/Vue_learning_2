<template>
  <div>
    <ul>
      <Person-info
        v-for="item in employees"
        :key="item.id"
        :id="item.id"
        :name="item.name"
        :salary="item.salary"
        :isVisible="item.isVisible"
        @show="toggleVisibility"
        @delete="removeEmployee"
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
  data() {
    return {
      employees: [
        { id: 1, name: "Bank", salary: 50000, isVisible: false },
        { id: 2, name: "Bow", salary: 20000, isVisible: false },
        { id: 3, name: "Belle", salary: 20000, isVisible: false },
        { id: 4, name: "Mergency", salary: 15000, isVisible: false },
        { id: 5, name: "Nam", salary: 500, isVisible: false },
      ],
    };
  },
  methods: {
    toggleVisibility(id) {
      this.employees = this.employees.map((item) =>
        item.id === id ? { ...item, isVisible: !item.isVisible } : item
      );
    },
    removeEmployee(id) {
      this.employees = this.employees.filter((item) => item.id !== id);
    },
  },
};
</script>

<style scoped>
</style>
