<template>
    <div>
        <TodoHeader />
        <TodoMain :taches="todos" />
        <TodoFooter />
    </div>
</template>

<script setup lang="ts">
import TodoHeader from './TodoHeader.vue';
import TodoMain from './TodoMain.vue';
import TodoFooter from './TodoFooter.vue';
import type {todolis}

interface Todo  {
    id: number,
    title: string,
    complete: boolean,
}
const todos: Todo[] = [
    {
        id: 1,
        title: 'Tache1',
        complete: false,
    },
    {
        id: 2,
        title: 'Tache2',
        complete: false,
    },
    {
        id: 3,
        title: 'Tache3',
        complete: false,
    },
];

</script>

<style scoped></style>