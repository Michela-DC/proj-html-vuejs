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

            <div class="demos-sale">
                <div class="demos">
                    <div class="icon">
                        <i class="fa-solid fa-folder-open"></i>
                    </div>
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
            <div class="question-row">
                <h2>Do you have a construction project we can help with?</h2>
                <button>get a free quote</button>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'SectionJumbotron'
}
</script>

<style lang="scss" scoped>

@import '../assets/scss/mixins.scss';
@import '../assets/scss/variables.scss';

.jumbo-container{
    height: 642px;
    background-image: url('../assets/images/home-slider-62528242.jpg');
    @include bg-image;
    @include flex-basics;
    // position: relative;

    .title-row{
        text-align: center;
        @include small-row;

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
        position: fixed;
        z-index: 20;
        top: 100px;
        right: 15px;

        .demos, .on-sale{
            background-color: white;
            width: 50px;
            height: 50px;
            border-radius: 5px;
            font-size: 0.625rem;
            text-align: center;
            display: flex;
            flex-direction: column;
            justify-content: center;
            font-weight: bold;
            box-shadow: 0px 0px 15px $gray-font;
        }

        .demos{
            margin-bottom: 5px;

            .icon{
                font-size: 1rem;
            }
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

// Question ------------------------------------

.question-container{
    background-color: $light-color;

    .question-row{
        @include small-row;
        margin: 0 auto;
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

}
    
</style>