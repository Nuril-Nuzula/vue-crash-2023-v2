<!-- eslint-disable prettier/prettier -->
<template>
  <header>
    <h1>{{ title }}</h1>
    <CustomButton @toggle-add-task="$emit('toggle-add-task')" text="Add Task" color="green" />
  </header>
</template>

<script>
import CustomButton from "./Button";

export default {
  name: "CustomHeader",
  props: {
    title: String,
  },
  components: {
    CustomButton,
  },
};
</script>
<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>
