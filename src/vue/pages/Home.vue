<script>
    export default {
        components: {
        },
    }
</script>

<template>
    <section class="hero-section">

        <div class="hero-title">
            <span>hi, i'm daniele. i am a</span>
            <span>creative</span>
            <span>electronics</span>
            <span>engineer</span>
        </div>

    </section>
</template>

<style lang="scss" scoped>
    @use 'src/scss/abstracts';

    .hero-section {
        .hero-title {
            text-transform: uppercase;
            display: grid;
            grid-template-areas:
                "t1 t2"
                "t3 t3"
                "t4 t4";


            span:nth-child(1) {
                grid-area: t1;
            }

            span:nth-child(2) {
                grid-area: t2;
            }

            span:nth-child(3) {
                grid-area: t3;
            }

            span:nth-child(4) {
                grid-area: t4;
            }
        }
    }
</style>