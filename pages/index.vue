<template>
    <div>
        <NuxtLayout :name="layout">
            <AppHeader/>
            <AppIntro />
            <AppAbout />
            <AppWhy/>
            <AppNFTIntro/>
            <AppSecondDrop/>
            <AppRoadMap/>
            <AppFaq/>
            <AppFooter/>
            
        </NuxtLayout>
    </div>
</template>

<script setup>
    import AppIntro from '../components/AppIntro.vue'
    import AppAbout from '../components/AppAbout.vue'

    definePageMeta({
        layout: false,
    });

    const layout = "default"
</script>