<template>
    <section class="section-3">
        <div class="container">
            <div class="cards-wrapper">
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
    name: 'SectionThree',
}
</script>

<style lang="scss" scoped>

@import '../assets/scss/mixins.scss';

.section-3{
    background-image: url('../assets/images/home-244125289.jpg');
    @include bg-image;
    position: relative;
    
    &::before{
        content: '';
        position: absolute;
        top: 0;
        width: 100%;
        height: 68px;
        background-color: white;
        background: radial-gradient(60% 68px at top, white 99%, transparent);
    }

    &::after{
        content: '';
        position: absolute;
        bottom: 0;
        width: 100%;
        height: 68px;
        background: radial-gradient(60% 68px at bottom, white 99%, transparent);
    }

    .container{
        height: 500px;
        @include flex-basics;

        .cards-wrapper{
            @include wrapper;
            display: flex;
            justify-content: space-between;

            .card{
                text-transform: uppercase;
                text-align: center;
                
                .icon, .number{
                    color: $light-color;
                    font-size: 2.875rem;
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

</style>