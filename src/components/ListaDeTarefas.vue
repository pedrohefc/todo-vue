<script setup>
    const props = defineProps(['tarefas']);
</script>

<template>
    <ul class="list-group mt-4">
        <li v-for="tarefa in props.tarefas" :key="tarefa.titulo" :class="['list-group-item', {done: tarefa.finalizada}]">
            <input v-model="tarefa.finalizada" :id="tarefa.titulo" type="checkbox">
            <label class="ms-3" :for="tarefa.titulo">
                {{ tarefa.titulo }}
            </label>
        </li>
    </ul>
</template>