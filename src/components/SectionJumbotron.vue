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

    .demos-sale{
        position: fixed;
        z-index: 20;
        top: 110px;
        right: 16px;

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

@media screen and (min-width: 549px) and (max-width: 729px){
    .jumbo-container .demos-sale{
        top: 150px;
    }
}

@media screen and (max-width: 548px){
    .jumbo-container .demos-sale{
        top: 190px;
    }
}
    
</style>