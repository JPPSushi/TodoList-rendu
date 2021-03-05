
<template>
  <div id="app">
    <TodoCard></TodoCard>
  </div>
</template>

<script>
import TodoCard from './components/TodoCard';


export default {
  name: 'app',
  components: {
    TodoCard
  }
}
</script>

<style>
body{
  width: 100vw;
  height: 100vh;
  background-color: orange;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>