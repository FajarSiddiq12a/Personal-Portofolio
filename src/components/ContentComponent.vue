<template>
    <div id="content" class="content relative sm:overflow-y-auto flex flex-col sm:gap-y-8 max-sm:gap-y-5 sm:py-12 px-5 h-full">
        <AboutComponent />
        <SkillComponent />
        <EducationComponent />
        <ExperienceComponent />
        <!-- <PortfolioComponent /> -->
        <ProjectComponent />
        <ContactComponent />
        <FooterComponent />
    </div>
</template>

<script>
import AboutComponent from './contents/AboutComponent.vue';
import SkillComponent from './contents/SkillComponent.vue';
import EducationComponent from './contents/EducationComponent.vue';
import ExperienceComponent from './contents/ExperienceComponent.vue';
// import PortfolioComponent from './contents/PortfolioComponent.vue';
import ProjectComponent from './contents/ProjectComponent.vue';
import ContactComponent from './contents/ContactComponent.vue';
import FooterComponent from './FooterComponent.vue';

export default {
    name: 'content-page',
    components: {
        AboutComponent,
        SkillComponent,
        EducationComponent,
        ExperienceComponent,
        // PortfolioComponent,
        ProjectComponent,
        ContactComponent,
        FooterComponent,
    }
}
</script>

<style lang="scss">
$bg-scrollbar: #29241e;
$color-scrollbar: #333230;
$color-scrollbar-hover: #303233;

.shadow-custom {
    box-shadow: 1px 6px 12px 2px rgba(0, 0, 0, .4);
}

.content {
    &::-webkit-scrollbar {
        width: 8px;
    }

    &::-webkit-scrollbar-track {
        background: $bg-scrollbar;
        border-radius: 5px;
    }

    &::-webkit-scrollbar-thumb {
        background-color: $color-scrollbar;
        border-radius: 8px;

        &:hover {
            background-color: $color-scrollbar-hover;
        }
    }
}
</style>