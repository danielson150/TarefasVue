<template>
    <div class="task-grid">
        <template v-if="tasks.length">
        <Task v-for="task in tasks" :key="task.name" :task="task"></Task> 
        </template>
        <p v-else>Sua vida está em dias :)</p>
    </div>
</template>

<script>
import Task from './Task.vue'
export default {
    components: {Task},
    props: {

        tasks: {type: Array, require: true}
    }
}
</script>

<style>

</style>
