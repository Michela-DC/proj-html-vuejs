<template>
  <section class="section-9">
      <div class="container">
            <div class="title-row">
                <h3 class="title">trusted partners</h3>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ducimus corrupti perferendis, aliquid asperiores voluptas sequi qui! Voluptatibus, commodi!</p>
            </div>

            <div class="partners-row">
                <figure class="logo-wrapper">
                    <img class="partners-logo" src="../assets/images/home-logo11-219096700-320x202.png" alt="">
                </figure>
                <figure class="logo-wrapper">
                    <img class="partners-logo" src="../assets/images/home-logo10-219096700-320x202.png" alt="">
                </figure>
                <figure class="logo-wrapper">
                    <img class="partners-logo" src="../assets/images/home-logo2-219096700-320x202.png" alt="">
                </figure>
                <figure class="logo-wrapper">
                    <img class="partners-logo" src="../assets/images/home-logo1-219096700-320x202.png" alt="">
                </figure>
                <figure class="logo-wrapper">
                    <img class="partners-logo" src="../assets/images/home-logo9-219096700-320x202.png" alt="">
                </figure>
            </div>
      </div>
  </section>
</template>
å
<script>
export default {
    name: 'SectionNine'
}
</script>

<style lang="scss" scoped>

@import '../assets/scss/mixins.scss';
@import '../assets/scss/variables.scss';

.container{
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 33px;
    padding: 80px 0;
}

@include reusable-title-row;

.partners-row{
    @include medium-row;
    display: flex;
    gap: 25px;

    .logo-wrapper{
        padding: 0 10px;

        .partners-logo{
            width: 100%;
            display: block;
        }
    }
}

</style>