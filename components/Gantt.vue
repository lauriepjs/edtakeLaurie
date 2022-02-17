<template>
  <div>
    <h1>Voici le Gantt</h1>
    <link rel="stylesheet" href="frappe-gantt.css" />
    <script src="dist/frappe-gantt.js"></script>
    <svg id="gantt"></svg>
  </div>
</template>

<script>
import Gantt from "frappe-gantt";

export default {
  name: "tasks",

  data() {
    return {
      tasks: [
        {
          id: "Task 1",
          name: "Candidater",
          start: "2022-2-9",
          end: "2022-4-15",
          progress: 100,
        },
        {
          id: "Task 2",
          name: "Envoyer un mail récapitulatif",
          start: "2022-4-14",
          end: "2022-8-14",
          progress: 100,
        },
      ],
    };
  },

  mounted() {
    this.gantt = new Gantt("#gantt", this.tasks, {
      view_mode: "Month",
      language: "fr",
    });
  },
};
</script>
