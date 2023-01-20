<template>
    <Head>
        <Title>
            Post {{ id }}
        </Title>
    </Head>
    <h2 >Bienvenido al Post numero #{{ id }}</h2>
</template>

<script setup>
    const id = useRoute().params.id;
    definePageMeta({ // Para validar que lo que pongan no sea inventado
        validate: async (route) => {
            const nuxtApp = useNuxtApp();

            return /^\S\w+$/.test(route.params.id);
        }
    })
</script>