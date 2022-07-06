<template>
  <header>
    <h1>{{ title }}</h1>
    <Button @click="onClick()" text="Add Task" color="green" />
  </header>
</template>


<script>
import Button from './Button.vue';

export default {
  name: "Header",
    // props: ['title']
  props: {
    title: {
      type: String,
      default: "Hello World"
    } 
  },
  components: {
    Button
  },
  methods: {
    onClick() {
      console.log('click');
    }
  }
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