<template>
    <div class="slide-right w-full rounded-md bg-background sm:p-5 max-sm:p-3 shadow-custom">
        <h1 class="sm:text-xl max-sm:text-lg font-semibold mb-3"><span class="text-title">My</span> Skill</h1>
        <p class="max-sm:text-sm">About my skill on</p>
        <div class="w-full flex flex-wrap gap-4 justify-start max-sm:justify-center items-center my-3">
            <div v-for="(skill, index) in skills" :key="index"
                class="sm:w-16 sm:h-16 max-sm:w-14 max-sm:h-14 rounded-md bg-black/60 text-white sm:text-4xl max-sm:text-2xl flex items-center justify-center transition-all duration-300 ease-in-out border border-black/60 hover:border-title hover:text-title">
                <span :class="skill.icon"></span>
            </div>
        </div>
        <p class="sm:text-sm mt-5">Support my skill on</p>
        <div class="w-full flex flex-wrap space-x-5 justify-start max-sm:justify-center items-center my-3">
            <div v-for="(support, index) in supports" :key="index"
                class="sm:w-16 sm:h-16 max-sm:w-14 max-sm:h-14 rounded-md bg-black/60 text-white sm:text-4xl max-sm:text-2xl flex items-center justify-center transition-all duration-300 ease-in-out border border-black/60 hover:border-title hover:text-title">
                <span :class="support.icon"></span>
            </div>
        </div>
    </div>
</template>

<script>

export default {
    name: 'skill-component',
    data() {
        return {
            skills: [
                { icon: 'mdi mdi-language-html5' },
                { icon: 'mdi mdi-language-css3' },
                { icon: 'mdi mdi-language-javascript' },
                { icon: 'mdi mdi-bootstrap' },
                { icon: 'mdi mdi-tailwind' },
                { icon: 'mdi mdi-vuejs' },
                { icon: 'mdi mdi-language-php' },
                { icon: 'mdi mdi-laravel' },
            ],
            supports: [
                { icon: 'mdi mdi-git' },
                { icon: 'mdi mdi-github' },
                { icon: 'mdi mdi-google-chrome' },
                { icon: 'mdi mdi-microsoft-visual-studio-code' },
                // {icon: 'mdi mdi-'},
            ]
        }
    }
}
</script>