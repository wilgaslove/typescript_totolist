<template>
    <footer class="footer">
        <span class="todo-count">
            <strong>{{ remaining }}</strong> tâche {{ remaining > 1 ? 's' : '' }} restante{{ 
                remaining > 1 ? 's' : '' }}
        </span >
        <ul class="">
            <li>
                <router-link to="#">Tous</router-link>
            </li>
            <li>
                <router-link to="#">En cours</router-link>
            </li>
            <li>
                <router-link to="#">Terminés</router-link>
            </li>
        </ul>

        <button class="clear-completed">Eff. tâches terminées</button>
    </footer>
</template>

<script setup lang="ts">
import {ref} from 'vue';

const remaining = ref(1)
</script>

<style scoped></style>