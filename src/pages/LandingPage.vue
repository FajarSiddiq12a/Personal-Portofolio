<template>
    <div
        class="relative w-full h-screen bg-background text-text grid sm:grid-cols-2 sm:gap-x-5 max-sm:grid-cols-1 max-sm:ga-y-3 sm:overflow-hidden max-sm:overflow-x-hidden">
        <PortfolioPage />
        <ContentPage />
    </div>
</template>

<script>
import PortfolioPage from '@/components/PortfolioComponent.vue';
import ContentPage from '@/components/ContentComponent.vue';

export default {
    name: 'landing-page',
    components: {
        PortfolioPage,
        ContentPage,
    }
}
</script>