<template>
  <MyCard>
    <template v-slot:card-header>
      <h1>Employees info</h1>
    </template>
    <template v-slot:card-button>
      <button @click="showDetail">More Detail</button>
      <button @click="deleteEmployee">Delete</button></template>
    <template v-slot:card-content
      ><div>
        <p v-show="isVisible">Name: {{ name }} | Salary: {{ salary }}</p>
      </div>
    </template>
  </MyCard>
</template>

<script>
import MyCard from "./MyCard.vue";
export default {
  name: "PersonInfo",
  components: {
    MyCard,
  },
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
MyCard {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 20px;
  text-align: center;
}

button {
  margin-right: 10px;
  margin-bottom: 10px;
  padding: 8px 16px;
  border: none;
  background-color: #4caf50;
  color: white;
  border-radius: 4px;
  cursor: pointer;
}

button:hover {
  background-color: #45a049;
}

h1 {
  margin: 10px;
}

p {
  margin-top: 10px;
  font-size: 16px;
}
</style>

