<template>
    <div class="list" :key="task" v-for="task in tasks">
        <input type="checkbox">
        <p>{{ task.name }}</p>
        <button><i class="fas fa-trash"></i></button>
    </div>
</template>
<script>
export default {
    name : 'TodoList',
    props: {
        tasks: {
            type: Array,
            default: () => []
        },
        name: {
            type: String
        }
    }

}
</script>

<style lang="css">
.list{
    display: flex;
    justify-content: space-between;
    padding: 20px;

}
</style>