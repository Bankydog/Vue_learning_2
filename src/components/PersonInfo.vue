<template>
  <div>
    <h1>Employees info</h1>
    <button @click="showDetail">More Detail</button>
    <button @click="deleteEmployee">Delete</button>
    <div>
      <p v-show="isVisible">Name: {{ name }} | Salary: {{ salary }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "PersonInfo",
  props: {
    id: {
      type: Number,
      required: true,
    },
    name: {
      type: String,
      required: true,
    },
    salary: {
      type: Number,
      default: 15000,
    },
    isVisible: {
      type: Boolean,
      default: false,
    },
  },
  methods: {
    showDetail() {
      this.$emit("show", this.id);
    },
    deleteEmployee() {
      this.$emit("delete", this.id);
    },
  },
};
</script>

<style scoped>
button {
  margin-right: 10px;
}

p {
  margin-top: 10px;
  font-size: 16px;
}
</style>
