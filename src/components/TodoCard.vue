<template>
    <body>
        <div class="card">
            <div class="header">
                <p>{{date}}</p>
                <p class="Tcolor">VueJs Tutorial ToDo List</p>
                <p>5 taches</p>
            </div>
            <NewTodo @newTask = "sendTask"></NewTodo>
            <TodoList v-bind:tasks="tasks"></TodoList>
        </div>
    </body>
        
    

</template>
<script>
import NewTodo from './NewTodo';
import TodoList from './TodoList';



export default {
    name: "TodoCard",
    components: {
            NewTodo,
            TodoList
        },
    data() {

        return {
            day: ["Lundi", "Mardi", "Mercredi", "Jeudi", "Vendredi", "Samedi", "Dimanche"],
            month: ["Janvier", "Février", "Mars", "Avril", "Mai", "Juin", "Juillet", "Août", "Septembre", "Octobre", "Novembre", "Décembre"],
            tasks: []
        }
        

    },
    computed: {

        date: function() {
            let today = new Date();
            let todate = today.getFullYear() + ' ' + `${this.month[(today.getMonth())]}` + ' ' + `${this.day[(today.getDate())-1]}`; 
            return todate; 
        }
        
    },
    methods: {
        sendTask( send ) {
            this.tasks.push({ name: send, state: 0 })
        }
    }
    
}

</script>

<style scoped>
.Tcolor{
    color: #42b983;
}
.card{
    width: 50vw;
    height: 50vh;
    background-color: white;
}
.header{
    width: 100%;
    display: flex;
    justify-content: space-between;

    
}
.header > p{
    padding: 10px;
}

</style>>

