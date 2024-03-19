<template>
    <div>
        <h1>Error encontrado</h1>
        <h3 data-v-inspector="error.vue:4:9">{{ error.statusCode }} - {{ error.statusMessage }};</h3>
        <button @click="handleError">Clean Errors</button>

    </div>

</template>

<script setup>

const route = useRoute();
        const {error}= defineProps({
            error: Object,
        });
const path = route.path === error.url ? "/" : route.path;
        const handleError = () =>{
            clearError({ redirect: path});
        };

</script>

<style scoped>

div{
    text-align: center;
}
</style>