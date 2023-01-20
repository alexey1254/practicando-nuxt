<template>
    <div>
        <h1>Error encontrado</h1>
        <h3>{{ error.statusCode }} - {{ error.statusMessage }}</h3>
        <button @click="handleError">Limpiar errores</button>
    </div>
</template>

<script setup>
const props = defineProps({
    error: Object
});

const handleError = () => {
    clearError({redirect: "/"})
}
</script>

<style scoped>
div {
    text-align: center;
}
</style>