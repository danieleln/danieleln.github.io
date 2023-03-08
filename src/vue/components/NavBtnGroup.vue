<script>
    import NavButton from './NavButton.vue'

    export default {
        components: {
            NavButton
        },
        data() {
            return {
                context: 'work'
            }
        },
        methods: {
            selectContext(ctx) {
                this.context = ctx
            }
        }
    } 
</script>

<template>
    <div class="px-4 py-4">
        <NavButton
            label="work"
            @click="selectContext('work')"
            :is-active="context == 'work'"
        />
        <NavButton 
            label="about"
            @click="selectContext('about')"
            :is-active="context == 'about'"
        />
        <NavButton 
            label="contact"
            @click="selectContext('contact')"
            :is-active="context == 'contact'"
        />
    </div>
</template>

<style lang="scss" scoped>
    @use 'src/scss/abstracts';
</style>
