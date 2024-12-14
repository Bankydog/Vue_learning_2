<template>
  <div>
    <p>
      name : {{ name }} salary: {{ salary }}
    </p>
  </div>
</template>

<script>
export default {
  name: "PersonInfo",
  data() {
    return {
    };
  },
  props: {
    name:{
      type:String,
      required:true
    },
    salary:{
      type:Number,
      default:15000
    }
  }
};
</script>

<style scoped>

</style>