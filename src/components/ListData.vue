<template>
  <div>
    <ul>
      <PersonInfo
        v-for="item in employees"
        :key="item.id"
        :id="item.id"
        :name="item.name"
        :salary="item.salary"
        :isVisible="item.isVisible"
        @show="$emit('update-visibility', item.id)"
        @delete="$emit('delete-employee', item.id)"
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
  props: {
    employees: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style>
</style>