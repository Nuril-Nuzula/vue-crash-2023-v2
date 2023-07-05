<template>
  <div :key="task.id" v-for="task in tasks">
    <CustomTask
      @toggle-reminder="$emit('toggle-reminder', task.id)"
      @delete-task="$emit('delete-task', task.id)"
      :task="task"
    />
  </div>
</template>

<script>
import CustomTask from "./Task";
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Tasks",
  props: {
    tasks: Array,
  },
  components: {
    CustomTask,
  },
  emits: ["delete-task", "toggle-reminder"],
};
</script>
