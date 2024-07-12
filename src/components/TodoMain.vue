<template>
    <main class="main"> 
        <ul class="todo-list">
            <div>
                <input type="text">
            </div>
            <li :class="{ completed: todo.complete}" v-for="todo in taches" :key="todo.id">
                {{ todo.title }}
            </li>
        </ul>
        
    </main>
</template>

<script setup lang="ts">
import type { Todo } from '@/@types';

interface Todo  {
    id: number,
    title: string,
    complete: boolean,
}
// const props = defineProps(['taches'])

const props = defineProps<{
    taches: Todo[]
}>();

</script>

<style scoped></style>