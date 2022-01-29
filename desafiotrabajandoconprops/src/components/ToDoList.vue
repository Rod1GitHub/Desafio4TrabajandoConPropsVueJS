<template>
  <ul>
    <li
      v-for="(taskArgument006, index006) in tasksPluralArray006"
      :key="index006"
    >
      <button @click="deleteTaskfromArrayMethod(index006)">
        Borrar del array
      </button>
      {{ taskArgument006 }}
    </li>
  </ul>
</template>

<script>
export default {
  name: "ToDoList",
  props: {
    tasksPluralArray006: [],
  },
  methods: {
    deleteTaskfromArrayMethod(indexParam) {
      this.tasksPluralArray006.splice(indexParam, 1);
    },
  },
};
</script>

<style></style>
