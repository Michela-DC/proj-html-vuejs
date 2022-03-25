<template>
    <section class="secion-values">
        <div class="container">

            <div class="title-row">
                <h3 class="title">our core values</h3>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ducimus corrupti perferendis, aliquid asperiores voluptas sequi qui! Voluptatibus, commodi!</p>
            </div>

            <div class="cards-row">
                <div class="card">
                    <div class="icon">
                        <i class="fa-solid fa-house-chimney"></i>
                    </div>
                    <div class="icon-title">great services</div>
                    <p>Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia</p>
                </div>

                <div class="card">
                    <div class="icon">
                        <i class="fa-solid fa-gear"></i>
                    </div>
                    <div class="icon-title">higher standards</div>
                    <p>Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia</p>
                </div>

                <div class="card">
                    <div class="icon">
                        <i class="fa-solid fa-users"></i>
                    </div>
                    <div class="icon-title">professional team</div>
                    <p>Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia</p>
                </div>

                <div class="card">
                    <div class="icon">
                        <i class="fa-regular fa-lightbulb"></i>
                    </div>
                    <div class="icon-title">creative solutions</div>
                    <p>Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia</p>
                </div>
            </div>

        </div>
    </section>
</template>

<script>
export default {
    name: 'SectionValue',
}
</script>

<style lang="scss" scoped>

@import '../assets/scss/mixins.scss';
@import '../assets/scss/variables.scss';
@import '../assets/scss/mixins_mediaqueries.scss';

.container{
    background-color: $light-gray;
    padding: 70px 20px 50px 20px;
    @include flex-basics;
    flex-direction: column;
    gap: 45px;
    //per coprire clip-path della section four:
    position: relative;
    z-index: 3;
}

@include reusable-title-row;

.cards-row{
    @include medium-row;
    display: flex;
    gap: 2%;

    .card{
    width: calc(94% / 4);
    @include flex-basics;
    flex-direction: column;
    text-align: center;
    gap: 12px;
    color: $gray-font;
    padding: 15px;

        .icon{
            font-size: 2.5rem;
            color: white;
            width: 80px;
            height: 80px;
            border-radius: 50%;
            @include flex-basics;

        }

        &:first-child .icon{
            background-color: #4EA4A5;
        }

        &:nth-child(2) .icon{
            background-color: #4E6DA5;
        }

        &:nth-child(3) .icon{
            background-color: #F6722A;
        }

        &:last-child .icon{
            background-color: #A7CF47;
        }

        .icon-title{
            text-transform: capitalize;
            position: relative;
            padding: 12px 0;
            margin-bottom: 4px;
            display: flex;
            justify-content: center;

            &::after{
                content: "";
                position: absolute;
                width: 15%;
                top: 100%;
                height: 0.125rem;
                color: $gray-font;
            }
        }

        &:hover{
            .icon-title{
                color: $light-color;
            }

            .icon{
                background-color: $light-color;
            }
        }
    }

}

@include cards-mediaquery;

</style>