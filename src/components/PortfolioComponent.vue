<template>
    <div class="w-full h-screen flex flex-col sm:items-start max-sm:items-center justify-center sm:px-20 max-sm:px-5">
        <figure class="rounded-full w-52 max-sm:w-48 h-52 max-sm:h-48 flex items-end justify-center mb-5">
            <img :src="img" alt="profil image"
                class="w-52 max-sm:w-48 h-52 max-sm:h-48 rounded-full bg-title border border-text" />
        </figure>
        <h1 class="font-bold sm:text-4xl max-sm:text-3xl sm:mb-1 max-sm:mb-2">Hi, I'm <span class="text-title">Fajar Shodiq</span></h1>
        <h2 class="font-bold text-2xl mb-3">Frontend Developer</h2>
        <p class="text-justify max-sm:text-center leading-relaxed max-sm:text-sm">"Menjadi seorang frontend developer bukan hanya berfokus kepada tampilan apa yang akan dibangun, akan tetapi juga harus memikirkan kepuasan dan ketertarikan dari user yang melihat hasil dari yang dibangun".</p>
        <ul class="flex items-center gap-x-5 mt-6">
            <li v-for="(icon, index) in icons" :key="index">
                <a :href="icon.link" target="_blank"
                    class="flex flex-col gap-y-1 justify-center items-center outline-none transition duration-300 ease-in-out hover:text-title focus:text-title">
                    <span :class="icon.i" class="sm:text-3xl max-sm:text-2xl"></span>
                    <span v-text="icon.title" class="sm:text-sm max-sm:text-xs max-sm:font-medium"></span>
                </a>
            </li>
        </ul>
    </div>
</template>

<script>
import Image from '@/assets/profil.jpeg';

export default {
    name: 'portfolio-page',
    data() {
        return {
            img: Image,
            icons: [
                { title: 'Whatsapp', link: 'https://api.whatsapp.com/send/?phone=6281265300022&text&type=phone_number&app_absent=0', i: 'mdi mdi-whatsapp' },
                { title: 'Facebook', link: 'https://www.facebook.com/moch.kaza.desky', i: 'mdi mdi-facebook' },
                { title: 'Instagram', link: 'https://www.instagram.com/kaza_desky/', i: 'mdi mdi-instagram' },
                { title: 'Github', link: 'https://github.com/kazadesky', i: 'mdi mdi-github' },
            ]
        }
    }

}
</script>