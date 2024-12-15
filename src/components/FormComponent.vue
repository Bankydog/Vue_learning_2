<template>
  <form @submit.prevent="subMitForm">
    <div class="form-control">
      <label for="emp-name">Enter Name</label>
      <input
        id="emp-name"
        type="text"
        v-model.trim="employee.name"
        placeholder="Enter employee name"
      />
    </div>
    <div class="form-control">
      <label for="emp-salary">Enter Salary</label>
      <input
        id="emp-salary"
        type="number"
        v-model.trim="employee.salary"
        placeholder="Enter salary"
        min="0"
      />
    </div>
    <div>
      <button type="submit">Save</button>
    </div>
  </form>
</template>
<script>
export default {
  name: "FormComponents",
  data() {
    return {
      employee: {
        name: "",
        salary: "",
      },
    };
  },
  methods: {
    subMitForm() {
      const newEmployee = {
        name: this.employee.name,
        salary: this.employee.salary,
      };
      this.$emit("save", newEmployee);
      this.employee.name = "";
      this.employee.salary = "";
    },
  },
};
</script>
<style scoped>
form {
  background: rgba(60, 179, 113, 0.5);
  border-radius: 15px;
  width: 280px;
  height: 100px;
  padding: 10px;
  margin: 10px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-between;
}
label {
  margin-right: 10px;
}
input {
  height: 20px;
  border-radius: 10px;
  text-align: center;
  margin: 5px;
}
button {
  width: 100px;
  height: 25px;
  border-radius: 10px;
  background: #bcd010;
}
</style>