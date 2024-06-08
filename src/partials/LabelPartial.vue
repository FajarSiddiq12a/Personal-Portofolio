<template>
    <div>
        <label :for="labelFor" :class="[classDefault, classLabel]">
            <slot></slot>
        </label>
    </div>
</template>

<script>
export default {
    name: 'label-partial',
    props: {
        labelFor: {
            type: String,
            required: true
        },
        classDefault: {
            type: String,
            default: 'mb-1 text-sm font-medium'
        }
    },

    setup() {
        const classLabel = 'block';

        return {
            classLabel,
        }
    }
}
</script>