<template>
  <footer>
    <div class="footer-container">
        <section class="main-section">
          <div class="row">

            <div class="col">
              <div class="card-wrapper">
                <figure>
                  logo
                  <img :src="aboutAvada.logo" alt="">
                </figure>

                <p>{{aboutAvada.info}}</p>

                <button>{{aboutAvada.button}}</button>
              </div>
            </div>

          </div>
          
        </section>

        <section class="secondary-section">

        </section>
    </div>
  </footer>
</template>

<script>
export default {
    name: 'FooterAbout',

    data () {
      return {
        aboutAvada: {
          logo: require('../assets/images/construction_logo.png'),
          info: 'We are specialists in the construction of unique and exclusive properties. Our work inspires. We pride ourselves on delivering outstanding quality and design for leading clients across the world.',
          button: 'learn more',
        }
      }
    }
}
</script>

<style lang="scss" scoped>

@import '../assets/scss/variables.scss';
@import '../assets/scss/mixins.scss';

.footer-container{
  min-height: 450px;
  position: relative;
  display: flex;
  flex-direction: column;
}

.main-section{
  background-color: $dark-color;
  height: 400px;

  .card{
    border: 1px solid red;
    margin-bottom: 10px;

    .title{
      color: $light-color;
      text-transform: uppercase;
    }

    .info-gray{
      color: $gray-font;
    }

    .info-white{
      color: white;
    }
  }
}

.secondary-section{
  flex-grow: 1;
  background-color: #121212;
}

</style>