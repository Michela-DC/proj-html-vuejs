<template>
    <section class="jumbotron">
        <div class="jumbo-container">
            <div class="title-row">
                <h1 class="main-title">Building inspiring spaces</h1>
                <h3 class="subtitle">we build inspiring residential & commercial spaces</h3>
                <div class="btn-container">
                    <button class="btn-explore">explore recent work</button>
                    <button class="btn-quote">get a quote today</button>
                </div>
            </div>
        </div>
        <DemosSales/>
    </section>
</template>

<script>

import DemosSales from './DemosSales.vue'

export default {
    name: 'SectionJumbotron',

    components: {
        DemosSales,
    }
}
</script>

<style lang="scss" scoped>

@import '../assets/scss/mixins.scss';
@import '../assets/scss/variables.scss';

.jumbotron{
    background-image: url('../assets/images/home-slider-62528242.jpg');
    @include bg-image;
}

.jumbo-container{
    height: 642px;
    padding: 20px;
    @include flex-basics;

    .title-row{
        text-align: center;

        .main-title{
            font-size: 2.875rem;
            text-transform: uppercase;
            color: white;
            margin-bottom: 20px;
        }
        
        .subtitle{
            color: $light-color;
            margin-bottom: 30px;
            font-size: 1.15rem;
        }

        .btn-container{
            button[class^="btn"]{
                @include btn-common;
                font-size: 0.9rem;
                font-weight: 300;
            }

            .btn-explore{
                margin-right: 15px;
                margin-bottom: 12px;
                @include btn-dark;
            }

            .btn-quote{
                @include btn-light;
            }
        }
    } //fine row
}
    
</style>