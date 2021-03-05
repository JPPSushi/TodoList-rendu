<template>
    <div class="addTodo">
        <input type="text" placeholder="New task" v-model="task">
        <button @click = "sendTask(task)">Ajouter</button>
    </div>
</template>
<script>

export default {
    name : 'NewTodo',
    methods: {
    sendTask: function(task) {
      if(task != null) {
        this.$emit('newTask', task)
      }
    }
  }
}


</script>

<style lang="css">
.addTodo{
    display: flex;
    justify-content: center;
}
.addTodo > input{
    margin: 10px;
    padding: 10px;
}
</style>