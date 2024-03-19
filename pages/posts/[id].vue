<template>
    <Head>
        <Title>Post{{ id }}</Title>
    </Head>
    <h2>Bienvenido al Post #{{ id }}</h2>

</template>


<script setup>



const {id} = useRoute().params;

if(!/^[0-9]+$/.test(id)){
    throw createError({statusCode: "500" , statusMessage: "Param Type is Invalid"})
}

// definePageMeta({
//     validate: async(route)=>{
//         const nuxtApp = useNuxtApp();

//         // Verificar si 'id' contiene solo dígitos
//         return /^[a-zA-Z]+$/.test(route.params.id);
//     },
// });
</script>
