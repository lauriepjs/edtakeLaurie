<template>
  <div>
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
				start: '2022-01-01',
				end: '2022-08-08',
				name: 'Redesign website',
				id: "Task 0",
				progress: 20
			},
			{
				start: '2022-02-03',
				end: '2022-02-06',
				name: 'Write new content',
				id: "Task 1",
				progress: 5,
				dependencies: 'Task 0'
			},
			{
				start: '2022-03-04',
				end: '2022-03-08',
				name: 'Apply new styles',
				id: "Task 2",
				progress: 10,
				dependencies: 'Task 1'
			},
			{
				start: '2022-03-08',
				end: '2022-03-09',
				name: 'Review',
				id: "Task 3",
				progress: 5,
				dependencies: 'Task 2'
			},
			{
				start: '2022-04-08',
				end: '2022-05-10',
				name: 'Deploy',
				id: "Task 4",
				progress: 0,
				dependencies: 'Task 2'
			},
			{
				start: '2022-05-11',
				end: '2022-06-11',
				name: 'Go Live!',
				id: "Task 5",
				progress: 0,
				dependencies: 'Task 4',
				custom_class: 'bar-milestone'
			},
			{
				start: '2022-01-05',
				end: '2022-08-12',
				name: 'Long term task',
				id: "Task 6",
				progress: 0
			}
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
