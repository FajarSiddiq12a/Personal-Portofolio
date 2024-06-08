<template>
    <div>
        <input :type="inputType" :id="inputId" :class="[classDefault, classInput]" v-bind="$attrs" />
    </div>
</template>

<script>
export default {
    name: 'input-partial',
    props: {
        inputType: {
            type: String,
            required: true
        },
        inputId: {
            type: String,
            required: true
        },
        classDefault: {
            type: String,
            default: 'border-2 border-background focus:border-title placeholder:text-sm text-sm'
        }
    },

    setup() {
        const classInput = 'outline-none w-full sm:h-12 max-sm:h-11 px-3 rounded-md transition-all duration-300 ease-in-out bg-black/50 text-white';

        return {
            classInput
        }
    }
}
</script>