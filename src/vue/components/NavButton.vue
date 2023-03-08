<script>
export default {
    props: {
        label: String,
        isActive: {
            type: Boolean,
            default: false
        },
    },
    click() {
        this.$emit('click')
    }
}
</script>

<template>
    <a
        href="#"
        class="fs-3 px-6 py-2"
        :class="{ active: isActive }"
    >
        <span class="px-2">{{ label }}</span>
    </a>
</template>

<style lang="scss" scoped>
    @use 'src/scss/abstracts' as abs;

    a {
        span {
            text-transform: uppercase;
            transition: all 100ms ease-in-out;
        }

        &:hover span {
            background-color: var(--color-fg);
            color: var(--color-bg);
        }
        
        &.active span {
            text-decoration: underline;
        }

    }
</style>
