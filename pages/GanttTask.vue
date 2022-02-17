<template>
  <div>
    <Navbar />
    <Gantt />
    <ToDoList />
  </div>
</template>
<script>
import Gantt from "../components/Gantt.vue";
import Navbar from "../components/Navbar.vue"
import ToDoList from "../components/ToDoList.vue"

export default {
  name: 'GanttPage'
}
</script>
