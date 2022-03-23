<template>
  <section class="section-four">
      <div class="container">
            <div class="title-row">
                <h3 class="title">explore recent work</h3>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ducimus corrupti perferendis, aliquid asperiores voluptas sequi qui! Voluptatibus, commodi!</p>
            </div>

            <div class="cards-row">
                <figure class="img-wrapper">
                    <img class="project-img" src="../assets/images/project2-featured-15013609-400x400.jpg" alt="">
                </figure>
                <figure class="img-wrapper">
                    <img class="project-img" src="../assets/images/project1-featured-294276386-400x400.jpg" alt="">
                </figure>
                <figure class="img-wrapper">
                    <img class="project-img" src="../assets/images/project3-featured-189023420-400x400.jpg" alt="">
                </figure>
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
    name: 'SectionFour'
}
</script>

<style lang="scss" scoped>

@import '../assets/scss/mixins.scss';
@import '../assets/scss/variables.scss';

.container{
    // height: 550px;
    padding: 50px 0 70px 0;
    @include flex-basics;
    flex-direction: column;
    gap: 55px;
}

@include reusable-title-row;

.cards-row{
    @include medium-row;
    display: flex;
    justify-content: space-between;
    gap: 2%;

    .img-wrapper{
        width: calc(96% / 3);
        
        .project-img{
            display: block;
            width: 100%;
        }
    }
}

.view-all-row{
    @include medium-row;
    @include flex-basics;
    position: relative;

    &::before{
        content: "";
        height: 2px;
        width: calc(96% / 3);
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
        width: calc(96% / 3);
        position: absolute;
        left: 0;
        top: 50%;
        transform: translate(0, -50%);
        border-radius: 50px;
        background-color: $light-gray;
    }

    .view-all{
        text-transform: uppercase;
        font-size: 0.875rem;

    }
}

</style>