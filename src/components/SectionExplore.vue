<template>
  <section class="section-explore">
      <div class="container">
            <div class="title-row">
                <h3 class="title">explore recent work</h3>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ducimus corrupti perferendis, aliquid asperiores voluptas sequi qui! Voluptatibus, commodi!</p>
            </div>

            <div class="cards-row">
                <div class="card">
                    <figure class="img-wrapper">
                        <img class="project-img" src="../assets/images/project2-featured-15013609-400x400.jpg" alt="">
                    </figure>

                    <div class="card-back">
                        <div class="icons-container">
                            <div class="icon-wrapper">
                                <i class="fa-solid fa-link"></i>
                            </div>
                            <div class="icon-wrapper">
                                <i class="fa-solid fa-magnifying-glass"></i>
                            </div>
                        </div>
                        <div>Florida health facility</div>
                        <div>commercial</div>
                    </div>
                </div>
                <div class="card">
                    <figure class="img-wrapper">
                        <img class="project-img" src="../assets/images/project1-featured-294276386-400x400.jpg" alt="">
                    </figure>

                    <div class="card-back">
                        <div class="icons-container">
                            <div class="icon-wrapper">
                                <i class="fa-solid fa-link"></i>
                            </div>
                            <div class="icon-wrapper">
                                <i class="fa-solid fa-magnifying-glass"></i>
                            </div>
                        </div>
                        <div>Maine Modernity</div>
                        <div>residential</div>
                    </div>
                </div>
                <div class="card">
                    <figure class="img-wrapper">
                        <img class="project-img" src="../assets/images/project3-featured-189023420-400x400.jpg" alt="">
                    </figure>

                    <div class="card-back">
                        <div class="icons-container">
                            <div class="icon-wrapper">
                                <i class="fa-solid fa-link"></i>
                            </div>
                            <div class="icon-wrapper">
                                <i class="fa-solid fa-magnifying-glass"></i>
                            </div>
                        </div>
                        <div>Exclusive Urban Living</div>
                        <div>commercial</div>
                    </div>
                </div>
            </div>

            <div class="view-all-row">
                <div class="view-all">
                    view all projects
                </div>
            </div>
      </div>
  </section>
</template>

<script>
export default {
    name: 'SectionExplore',
}
</script>

<style lang="scss" scoped>

@import '../assets/scss/mixins.scss';
@import '../assets/scss/variables.scss';
@import '../assets/scss/mixins_Hover.scss';

.container{
    // height: 550px;
    padding: 50px 20px 85px 20px;
    @include flex-basics;
    flex-direction: column;
    gap: 40px;
    //per coprire clip-path della section four:
    position: relative;
    z-index: 3;
}

@include reusable-title-row;

.cards-row{
    @include medium-row;
    @include flex-basics;
    display: flex;
    gap: 2.8%;

    .card{
        position: relative;

        .img-wrapper{
            .project-img{
                display: block;
                width: 100%;
            }
        }
    }

}

@include hover_section-explore;

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
        background-color: $light-gray;
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
        background-color: $light-gray;
    }

    .view-all{
        text-transform: uppercase;
        font-size: 0.78rem;
        color: $gray-font;
    }
}

@include cards-img-mediaquery;

</style>