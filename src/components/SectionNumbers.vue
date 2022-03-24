<template>
    <section class="section-numbers">
        <div class="container">
            <div class="cards-row">
                <div class="card">
                    <div class="icon">
                        <i class="fa-solid fa-suitcase"></i>
                    </div>
                    <div class="number">3534</div>
                    <div class="info">planning applications</div>
                </div>

                <div class="card">
                    <div class="icon">
                        <i class="fa-regular fa-building"></i>
                    </div>
                    <div class="number">896</div>
                    <div class="info">completed projects</div>
                </div>

                <div class="card">
                    <div class="icon">
                        <i class="fa-solid fa-users"></i>
                    </div>
                    <div class="number">172</div>
                    <div class="info">trained professionals</div>
                </div>

                <div class="card">
                    <div class="icon">
                        <i class="fa-solid fa-globe"></i>
                    </div>
                    <div class="number">19</div>
                    <div class="info">international offices</div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'SectionNumbers',
}
</script>

<style lang="scss" scoped>

@import '../assets/scss/mixins.scss';

.section-numbers{
    background-image: url('../assets/images/home-244125289.jpg');
    @include bg-image;
    position: relative;
    
    &::before{
        content: "";
        position: absolute;
        bottom: 72%;
        width: 100%;
        height: 500px;
        background-color: white;
        -webkit-clip-path: ellipse(60% 30% at 50% 50%);
        clip-path: ellipse(68% 35% at 50% 50%);
    }

    &::after{
        content: "";
        position: absolute;
        top: 72%;
        width: 100%;
        height: 500px;
        background-color: white;
        -webkit-clip-path: ellipse(60% 30% at 50% 50%);
        clip-path: ellipse(68% 35% at 50% 50%);
    }

    .container{
        padding: 175px 20px;
        @include flex-basics;

        .cards-row{
            @include medium-row;
            display: flex;
            justify-content: space-between;

            .card{
                text-transform: uppercase;
                text-align: center;
                padding: 10px;
                
                .icon, .number{
                    color: $light-color;
                    font-size: 3rem;
                }
                .info{
                    padding-top: 8px;
                    color: white;
                    font-size: 0.875rem;
                }
            }
        }
    }
}

@include cards-mediaquery;

@media screen and (max-width: 575px){
    .section-numbers{
    
        &::before{
            bottom: 80%;
        }

        &::after{
            top: 80%;
        }
    }

}

</style>