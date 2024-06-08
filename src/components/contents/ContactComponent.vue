<template>
    <div class="slide-right w-full rounded-md bg-background sm:p-5 max-sm:p-3 shadow-custom">
        <h1 class="sm:text-xl max-sm:text-lg font-semibold mb-3"><span class="text-title">Contact</span> With Me</h1>
        <form @submit.prevent="resetForm" class="grid sm:grid-cols-2 max-sm:grid-col-1 sm:gap-x-5 pb-5">
            <div class="sm:col-span-1 max-sm:col-span-2 sm:mb-4 max-sm:mb-3">
                <label-partial label-for="name">Your Name</label-partial>
                <input-partial input-type="text" input-id="name" required />
            </div>
            <div class="sm:col-span-1 max-sm:col-span-2 sm:mb-4 max-sm:mb-3">
                <label-partial label-for="phone">Number Phone</label-partial>
                <input-partial input-type="number" input-id="phone" required />
            </div>
            <div class="col-span-2 sm:mb-4 max-sm:mb-3">
                <label-partial label-for="email">Email</label-partial>
                <input-partial input-type="email" input-id="email" required />
            </div>
            <div class="col-span-2 sm:mb-4 max-sm:mb-3">
                <label-partial label-for="subject">Subject</label-partial>
                <input-partial input-type="text" input-id="subject" required />
            </div>
            <div class="col-span-2 sm:mb-4 max-sm:mb-3">
                <label-partial label-for="message">Your Message</label-partial>
                <textarea id="message"
                    class="w-full bg-black/50 rounded-md sm:min-h-32 max-sm:min-h-28 p-3 border-2 border-background transition duration-300 ease-in-out focus:border-title outline-none text-sm"
                    required></textarea>
            </div>
            <div class="col-span-1">
                <button-partial button-type="submit">Send to submit</button-partial>
            </div>
        </form>
    </div>
</template>

<script>
import LabelPartial from '@/partials/LabelPartial.vue';
import InputPartial from '@/partials/InputPartial.vue';
import ButtonPartial from '@/partials/ButtonPartial.vue';

export default {
    name: 'contact-component',
    components: {
        LabelPartial,
        InputPartial,
        ButtonPartial
    }
}
</script>