<template>
    <div>
        <NuxtLayout :name="layout">
            <AppIntro />
        </NuxtLayout>
    </div>
</template>

<script setup>
    import AppIntro from '../components/AppIntro.vue'

    definePageMeta({
        layout: false,
    });

    const layout = "default"
</script>