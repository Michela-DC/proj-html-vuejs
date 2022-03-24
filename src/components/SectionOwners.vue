<template>
  <section class="section-owners">
      <div class="container">
            <div class="row">
                <h3 class="title">Our home owners say</h3>

                <figure class="owner-img">
                    <img class="owner-photo" src="../assets/images/home-testimonial-113165296.jpg" alt="">
                </figure>

                <p class="owner-says">
                    “No man but feels more of a man in the world if he have but a bit of ground that he can call his own. However small it is on the surface, it is four thousand miles deep; and that is a very handsome property.”
                </p>

                <div class="owner-name">
                    <div class="name">Jane Smith</div>
                    <div class="role">new home owner</div>
                </div>
            </div>
      </div>
  </section>
</template>

<script>
export default {
    name: 'SectionOwners'
}
</script>

<style lang="scss" scoped>

@import '../assets/scss/mixins.scss';
@import '../assets/scss/variables.scss';

.section-owners{
    background-image: url('../assets/images/home-parallax-144609983.jpg');
    @include bg-image;
    position: relative;
    
    &::before{
        content: "";
        position: absolute;
        bottom: 75%;
        width: 100%;
        height: 500px;
        background-color: $light-gray;
        -webkit-clip-path: ellipse(60% 30% at 50% 50%);
        clip-path: ellipse(68% 35% at 50% 50%);
    }

    &::after{
        content: "";
        position: absolute;
        top: 75%;
        width: 100%;
        height: 500px;
        background-color: $light-gray;
        -webkit-clip-path: ellipse(60% 30% at 50% 50%);
        clip-path: ellipse(68% 35% at 50% 50%);
    }
}

.container{
    display: flex;
    justify-content: center;
    padding: 150px 20px;

    .row{
        @include small-row;
        @include flex-basics;
        flex-direction: column;
        gap: 25px;
        text-align: center;
        color: white;

        .title{
            position: relative;
            display: flex;
            justify-content: center;
            padding-bottom: 15px;
            font-size: 1.5rem;

            &::after{
                content: "";
                position: absolute;
                width: 150px;
                top: 100%;
                height: 0.125rem;
                background-color: $light-color;
            }
        }

        .owner-img{
            border-radius: 50%;
            overflow: hidden;
            height: 120px;
            width: 120px;

            .owner-photo{
                display: block;
                width: 100%;
            }
        }

        .owner-says{
            font-style: italic;
        }

        .owner-name{
            text-transform: uppercase;
            font-weight: bold;
            font-size: 0.875rem;
            display: flex;
            gap: 15px;

            .name{
                position: relative;
                padding-right: 10px;

                &::after{
                    content: "";
                    position: absolute;
                    left: 100%;
                    top: 50%;
                    transform: translate(0, -50%);
                    display: block;
                    height: 5px;
                    width: 5px;
                    background-color: white;
                    border-radius: 50%;
                }
            }
            
        }
    }
}

</style>