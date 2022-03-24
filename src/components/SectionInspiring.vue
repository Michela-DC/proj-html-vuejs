<template>
    <section class="section-inspiring">
        <div class="container">
            <div class="row">
                <div class="title-col">
                    <h3 class="title">Building inspiring spaces</h3>
                    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Cumque, aperiam hic a beatae consequatur quae.</p>
                </div>
                <div class="button-col">
                    <button class="btn-quote">get a free quote</button>
                    <div class="few-seconds">Only takes a few seconds!</div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'SectionInspiring'
}
</script>

<style lang="scss" scoped>

@import '../assets/scss/mixins.scss';
@import '../assets/scss/variables.scss';

.section-inspiring{
    background-image: url('../assets/images/about-call-to-action-57862405.jpg');
    background-position-y: 82%;
    background-size: cover;
}

.container{
    padding: 95px 20px;
    @include flex-basics;
    position: relative;

    &::after{
        content: '';
        display: block;    
        position: absolute;
        bottom: 0;
        width: 100%;
        height: 30px;
        background-image: url('../assets/images/about-call-to-action-57862405.jpg');
        background-position-y: 73%;
        background-size: cover;
    }
}

.row{
    @include medium-row;
    display: flex;
    justify-content: space-between;

    .title-col{
        width: 65%;
        color: white;

        .title{
            position: relative;
            padding-bottom: 18px;
            font-size: 1.5rem;

            &::after{
                content: "";
                position: absolute;
                width: 150px;
                top: 100%;
                left: 0;
                height: 0.125rem;
                background-color: $light-color;
            }
        }

        p{
            padding-top: 20px;
            font-size: 1rem;
        }
    }

    .button-col{
        padding: 10px;
        text-align: center;

        .btn-quote{
            @include btn-light;
            @include btn-common;
            font-size: 1rem;
            margin-bottom: 12px;
        }

        .few-seconds{
            font-size: 0.75rem;
            color: white;
        }
    }
}

@media screen and (max-width: 768px){
    .row{
        flex-wrap: wrap;
        justify-content: center;
        gap: 20px;

        .title-col{
            text-align: center;

            .title{
                &::after{
                    left: 50%;
                    transform: translate(-50%);
                }
            }

        }
    }
}

</style>