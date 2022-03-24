<template>
  <section class="section-news">
      <div class="container">
            <div class="title-row">
                <h3 class="title">Latest news</h3>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ducimus corrupti perferendis, aliquid asperiores voluptas sequi qui! Voluptatibus, commodi!</p>
            </div>

            <div class="cards-row">
                <div class="card">
                    <figure class="img-wrapper">
                        <img class="project-img" src="../assets/images/blog-post-134132600-200x121.jpg" alt="">

                        <div class="card-back">
                            <div class="icons-container">
                                <div class="icon-wrapper">
                                    <i class="fa-solid fa-link"></i>
                                </div>
                                <div class="icon-wrapper">
                                    <i class="fa-solid fa-magnifying-glass"></i>
                                </div>
                            </div>
                            <div>Redeveloping</div>
                            <p>All about architectures and construction</p>
                        </div>
                    </figure>



                    <div class="card-info">
                        <div class="title-wrapper">
                            <h3 class="title">Redeveloping Florida’s Remote Southern Coast</h3>
                            <div class="date">December 7th, 2015</div>
                        </div>
                        <div class="paragraph">
                            Technology is Here to Stay Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus purus nisl, elementum vitae consequat at, tristique ut enim. Sed ut dignissim leo. Nullam sed metus id sapien faucibus rhoncus sed
                        </div>
                    </div>
                </div>

                <div class="card">
                    <figure class="img-wrapper">
                        <img class="project-img" src="../assets/images/blog-post-92486644-400x241.jpg" alt="">

                        <div class="card-back">
                            <div class="icons-container">
                                <div class="icon-wrapper">
                                    <i class="fa-solid fa-link"></i>
                                </div>
                                <div class="icon-wrapper">
                                    <i class="fa-solid fa-magnifying-glass"></i>
                                </div>
                            </div>
                           <div>Redeveloping</div>
                            <p>All about architectures and construction</p>
                        </div>
                    </figure>

                    <div class="card-info">
                        <div class="title-wrapper">
                            <h3 class="title">How We Manage Large Construction Projects</h3>
                            <div class="date">December 7th, 2015</div>
                        </div>
                        <div class="paragraph">
                            Technology is Here to Stay Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus purus nisl, elementum vitae consequat at, tristique ut enim. Sed ut dignissim leo. Nullam sed metus id sapien faucibus rhoncus sed
                        </div>
                    </div>
                </div>

                <div class="card">
                    <figure class="img-wrapper">
                        <img class="project-img" src="../assets/images/blog-post-332773904-400x241.jpg" alt="">
                        
                        <div class="card-back">
                            <div class="icons-container">
                                <div class="icon-wrapper">
                                    <i class="fa-solid fa-link"></i>
                                </div>
                                <div class="icon-wrapper">
                                    <i class="fa-solid fa-magnifying-glass"></i>
                                </div>
                            </div>
                            <div>Redeveloping</div>
                            <p>All about architectures and construction</p>
                        </div>
                    </figure>

                    <div class="card-info">
                        <div class="title-wrapper">
                            <h3 class="title">Future proofing a modern home</h3>
                            <div class="date">December 7th, 2015</div>
                        </div>
                        <div class="paragraph">
                            Technology is Here to Stay Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus purus nisl, elementum vitae consequat at, tristique ut enim. Sed ut dignissim leo. Nullam sed metus id sapien faucibus rhoncus sed
                        </div>
                    </div>
                </div>
            </div>

            <div class="view-all-row">
                <div class="view-all">
                    view all articles
                </div>
            </div>
      </div>
  </section>
</template>

<script>
export default {
    name: 'SectionNews'
}
</script>

<style lang="scss" scoped>

@import '../assets/scss/mixins.scss';
@import '../assets/scss/variables.scss';

.section-news{
    background-color: $light-gray;

    .container{
        // height: 550px;
        padding: 40px 20px 85px 20px;
        @include flex-basics;
        flex-direction: column;
        gap: 40px;
        //per coprire clip-path della section four:
        position: relative;
        z-index: 3;
    }
}

@include reusable-title-row;

.cards-row{
    @include medium-row;
    display: flex;
    justify-content: center;
    gap: 2.8%;

    .card{
        // width: calc(96% / 3);
        .img-wrapper{
            position: relative;
            position: relative;

            .project-img{
                display: block;
                width: 100%;
            }
        }

        .card-info{
            background-color: white;
            font-size: 0.78rem;
            color: $gray-font;
            padding: 28px 18px 18px 18px;
            line-height: 1.688rem;

            .title-wrapper{
                padding-bottom: 10px;
                position: relative;

                .title{
                    font-size: 1.25rem;
                }

                &::after{
                    content: "";
                    position: absolute;
                    width: 100%;
                    top: 100%;
                    height: 1px;
                    background-color: $light-gray;
                }
            }

            .paragraph{
                padding-top: 12px;
            }
        } //fine card-info
    }//fine card
}

.card-back{
    position: absolute;
    top: 0;
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    background-color: $light-color;
    color: white;
    visibility: hidden;
    text-align: center;
    padding: 10px;

    .icons-container{
        display: flex;
        gap: 5px;

        .icon-wrapper{
            width: 40px;
            height: 40px;
            border-radius: 100%;
            @include flex-basics;
            background-color: white;
            color: $light-color;
            margin: 5px;
            font-size: 1.3rem;
        }

    }

    p:last-child{
        font-size: 0.8rem;
    }
}

.card:hover .card-back{
    visibility: visible;
}

.view-all-row{
    @include medium-row;
    @include flex-basics;
    position: relative;

    &::before{
        content: "";
        height: 2px;
        width: calc(94.4% / 3);
        position: absolute;
        right: 0;
        top: 50%;
        transform: translate(0, -50%);
        border-radius: 50px; 
        background-color: white;
    }

    &::after{
        content: "";
        height: 2px;
        width: calc(94.4% / 3);
        position: absolute;
        left: 0;
        top: 50%;
        transform: translate(0, -50%);
        border-radius: 50px;
        background-color: white;
    }

    .view-all{
        text-transform: uppercase;
        font-size: 0.78rem;
        color: $gray-font;
    }
}

@include cards-img-mediaquery;

</style>