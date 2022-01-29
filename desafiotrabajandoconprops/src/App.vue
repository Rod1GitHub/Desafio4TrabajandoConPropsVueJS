<template>
  <div id="app-trabajando-con-props">
    <h2>Tarea</h2>
    <input type="text" v-model="taskSingularInput006" />
    <button @click="captureInputAndAddToEndOfArrayMethod006">
      Capturar y agregar al array
    </button>
    <ToDoListComponent006 v-bind:tasksPluralArray006="tasksPluralArray006" />
  </div>
</template>

<script>
import ToDoListComponent006 from "@/components/ToDoList.vue";
export default {
  name: "App",
  components: {
    ToDoListComponent006,
  },
  data() {
    return {
      taskSingularInput006: "",
      tasksPluralArray006: [],
    };
  },
  methods: {
    captureInputAndAddToEndOfArrayMethod006() {
      let { taskSingularInput006 } = this; // Esto captura el input
      this.tasksPluralArray006.push(taskSingularInput006); // push() lo envía al final del array
    },
  },
};
</script>

<style>
#app {
  font-family: Arial;
}
</style>
