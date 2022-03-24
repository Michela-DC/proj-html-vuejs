<template>
        <section class="section-specialists">
            <div class="container">

                <div class="title-row">
                    <h3 class="title">specialists in modern construction</h3>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ducimus corrupti perferendis, aliquid asperiores voluptas sequi qui! Voluptatibus, commodi!</p>
                </div>

                <div class="cards-row">
                    <div class="card" v-for="card in cards" :key="card.id">
                        <div v-if="card.icon" class="icon front">
                            <i :class="card.icon"></i>
                        </div>

                        <div v-if="card.titleFront" class="title front">
                            {{card.titleFront}}
                        </div>
                        <div v-if="card.titleBack" class="title back">
                            {{card.titleBack}}
                        </div>

                        <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Aperiam, sapiente!</p>

                        <button v-if="card.button" class="btn-quote back">
                            {{card.button}}
                        </button>
                    </div>
                </div>

            </div>
        </section>
</template>

<script>
export default {
    name: 'SectionSpecialists',

    data () {
        return {
            cards: [
                {   id: '1',   
                    icon: 'fa-regular fa-building',
                    titleFront: 'Buildings',
                    titleBack: 'Artfully Crafted',
                    button: 'get a quote'
                },
                {   id: '2',
                    icon: 'fa-solid fa-rotate',
                    titleFront: 'Renovate',
                    titleBack: 'Freshly New',
                    button: 'get a quote'
                },
                {   id: '3',
                    icon: 'fa-solid fa-house-chimney',
                    titleFront: 'Construct',
                    titleBack: 'perfect lines',
                    button: 'get a quote'
                },
                {   id: '4',
                    icon: 'fa-solid fa-truck',
                    titleFront: 'Exclusive',
                    titleBack: 'planning',
                    button: 'get a quote'
                }
            ],
        }
    },
    
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
        padding: 30px 18px;

        .icon{
            border: 1px solid $gray-font;
            width: 45px;
            height: 45px;
            border-radius: 50%;
            @include flex-basics;
        }

        .title.back{
            text-transform: uppercase;
        }

        .btn-quote{
            @include btn-common;
            background-color: rgba(255, 255, 255, 0.5);
            color: $gray-font;
        }

        .back{
            display: none;
        }

        &:hover{
            background-color: $light-color;

            .front{
                display: none;
            }

            .back{
                display: block;


            }
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

    .container{
        padding-bottom: 0;
    }

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