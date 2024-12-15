<template>
  <div>
    <h1>Employee's Data</h1>
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
h1 {
}
</style>

