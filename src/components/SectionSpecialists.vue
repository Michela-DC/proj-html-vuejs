<template>
        <section class="section-specialists">
            <div class="container">

                <div class="title-row">
                    <h3 class="title">specialists in modern construction</h3>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ducimus corrupti perferendis, aliquid asperiores voluptas sequi qui! Voluptatibus, commodi!</p>
                </div>

                <div class="cards-row">
                    <div class="card">
                        <div class="icon">
                            <i class="fa-regular fa-building"></i>
                        </div>
                        <h3>Buildings</h3>
                        <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Aperiam, sapiente!</p>
                    </div>

                    <div class="card">
                        <div class="icon">
                            <i class="fa-solid fa-rotate"></i>
                        </div>
                        <h3>Renovate</h3>
                        <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Aperiam, sapiente!</p>
                    </div>

                    <div class="card">
                        <div class="icon">
                            <i class="fa-solid fa-house-chimney"></i>
                        </div>
                        <h3>Construct</h3>
                        <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Aperiam, sapiente!</p>
                    </div>

                    <div class="card">
                        <div class="icon">
                            <i class="fa-solid fa-truck"></i>
                        </div>
                        <h3>Exclusive</h3>
                        <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Aperiam, sapiente!</p>
                    </div>
                </div>

            </div>
        </section>
</template>

<script>
export default {
    name: 'SectionSpecialists'
}
</script>

<style lang="scss" scoped>

@import '../assets/scss/mixins.scss';
@import '../assets/scss/variables.scss';

.container{
    @include flex-basics;
    padding: 100px 20px 80px 20px;
    flex-direction: column;
    gap: 55px;
    //per coprire clip-path della section four:
    position: relative;
    z-index: 3;
}

@include reusable-title-row;

.cards-row{
    border: 1px solid red;
    width: 82%;
    display: flex;
    @include flex-basics;
    gap: 2%;

    .card{
        width: calc(94% / 4);
        @include flex-basics;
        flex-direction: column;
        text-align: center;
        gap: 10px;
        font-size: 1.25rem;
        color: $gray-font;
        background-color: $light-gray;
        border-radius: 10px;
        padding: 30px 12px;

        .icon{
            border: 1px solid $gray-font;
            width: 45px;
            height: 45px;
            border-radius: 50%;
            @include flex-basics;
        }
    }
}

@media screen and (min-width: 769px) and (max-width: 992px){
    .cards-row{
        width: 95%;
    }
}

@media screen and (min-width: 576px) and (max-width: 768px){
    .cards-row{
        width: 100%;
        flex-wrap: wrap;

        .card{
            width: calc(94% / 2);
            margin-bottom: 20px;
        }
    }
}

@media screen and (max-width: 575px){
    .cards-row{
        width: 100%;
        flex-wrap: wrap;

        .card{
            width: 100%;
            margin-bottom: 20px;
        }
    }
}

</style>