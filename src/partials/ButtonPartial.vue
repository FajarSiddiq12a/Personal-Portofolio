<template>
    <div>
        <button :type="buttonType" :class="[classDefault, buttonClass]" v-bind="$attrs">
            <slot></slot>
        </button>
    </div>
</template>

<script>

export default {
    name: 'ButtonPartial',
    props: {
        buttonType: {
            type: String,
            default: 'button'
        },
        classDefault: {
            type: String,
            default: 'w-40 h-11 flex items-center justify-center bg-black/50 text-text rounded-md hover:text-title focus:text-title text-sm border border-background hover:border-title focus:border-title'
        }
    },
    setup() {
        const buttonClass = 'outline-none transition duration-300 ease-in-out font-medium shadow-lg';

        return {
            buttonClass,
        };
    }
};
</script>