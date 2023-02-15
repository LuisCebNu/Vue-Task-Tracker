<template>
  <header>
    <h1>{{ title }}</h1>
    <Button
      @btn-click="$emit('toggle-add-task')"
      :text="showTask ? 'Close' : 'Add Task'"
      :color="showTask ? 'red' : 'green'"
    />
  </header>
</template>

<script>
import Button from "./button";

export default {
  name: "Header",
  props: {
    title: String,
    showTask: Boolean,
  },
  components: {
    Button,
  },
};
</script>

<style lang="stylus" scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>