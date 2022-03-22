<template>
    <section class="jumbotron">
        <div class="jumbo-container">
            <div class="title-wrapper">
                <h1 class="main-title">Building inspiring spaces</h1>
                <h3 class="subtitle">we build inspiring residential & commercial spaces</h3>
                <div class="btn-wrapper">
                    <button class="btn-explore">explore recent work</button>
                    <button class="btn-quote">get a quote today</button>
                </div>
            </div>

            <div class="demos-sale">
                <div class="demos">
                    <div class="icon">icona</div>
                    <div>Demos</div>
                </div>
                <div class="on-sale">
                    <div class="sale-price">
                        <span class="dollar">$</span>
                        <span class="number">39</span>
                    </div>
                    <div>On Sale</div>
                </div>
            </div>
        </div>

        <div class="question-container">
            <h2>Do you have a construction project we can help with?</h2>
            <button>get a free quote</button>
        </div>
    </section>
</template>

<script>
export default {
    name: 'JumbotronAvada'
}
</script>

<style lang="scss" scoped>

@import '../assets/scss/mixins.scss';
@import '../assets/scss/variables.scss';

.jumbo-container{
    height: 642px;
    background-image: url('../assets/images/home-slider-62528242.jpg');
    background-position: center;
    background-repeat: no repeat;
    background-size: cover;
    @include flex-basics;
    position: relative;

    .title-wrapper{
        text-align: center;

        .main-title{
            font-size: 2.875rem;
            text-transform: uppercase;
            color: white;
            margin-bottom: 20px;
        }
        
        .subtitle{
            color: $light-color;
            margin-bottom: 30px
        }

        .btn-wrapper{
            button[class^="btn"]{
                @include btn-common;
                font-size: 0.9rem;
                font-weight: 300;
                padding: 12px 30px;
            }

            .btn-explore{
                margin-right: 12px;
                @include btn-dark;
            }

            .btn-quote{
                @include btn-light;
            }
        }
    } //fine css jumbo-wrapper

    .demos-sale{
        position: absolute;
        top: 10px;
        right: 10px;

        .demos, .on-sale{
            background-color: white;
            width: 48px;
            height: 48px;
            border-radius: 5px;
            font-size: 0.625rem;
            text-align: center;
            display: flex;
            flex-direction: column;
            justify-content: center;
            font-weight: bold;
        }

        .demos{
            margin-bottom: 5px;
        }

        .on-sale{
            .sale-price{
                font-size: 1.125rem;
                color: #53aa53;
                position: relative;
                margin-bottom: 3px;
                

                .dollar{
                    position: absolute;
                    top: 3px;
                    font-size: 0.75rem;
                }

                .number{
                    margin-left: 7px;
                }
            }
        }
    }
}

.question-container{
    background-color: $light-color;
    min-height: 130px;
    display: flex;
    justify-content: center;
    position: relative;
    padding-top: 45px;

    button{
        @include btn-dark;
        @include btn-common;
        // padding: 10px 25px;
        text-transform: uppercase;
        border: 2px solid white;
        font-size: 0.875rem;
        position: absolute;
        top: 80%;
        left: 50%;
        transform: translate(-50%);
    }
}
    
</style>