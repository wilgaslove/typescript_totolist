<template>
    <main class="main"> 
        <ul class="todo-list">
            <li v-for="todo in taches" :key="todo.id">
                {{ todo.title }}
            </li>
        </ul>
        
    </main>
</template>

<script setup lang="ts">

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