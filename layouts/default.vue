<template>
    <div :class="'bg-[#121328]'">
        <AppHeader />
        <slot />
        <AppFooter />
    </div>
</template>

<script setup>
    import AppHeader from './components/AppHeader.vue'
    import AppFooter from './components/AppFooter.vue'
</script>