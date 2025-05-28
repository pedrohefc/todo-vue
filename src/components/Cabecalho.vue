<script setup>
defineProps({
    estado: Object
})
</script>

<template>
    <header class="p-5 mb-4 mt-4 bg-light rounded-3">
        <h1>Minhas tarefas</h1>
        <p>
            Você possui {{ estado.tarefas.filter(t => !t.finalizada).length }} tarefas pendentes
        </p>
    </header>
</template>