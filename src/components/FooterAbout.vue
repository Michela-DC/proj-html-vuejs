<template>
  <footer>
      <div class="footer-container">
          <section class="main-section">
            <div class="container">
                <div class="card" v-for="(item, i) in aboutAvada" :key="i">
                    <figure class="logo-wrapper" v-if="aboutAvada[i].logo">
                        <img :src="aboutAvada[i].logo" alt=""> 
                    </figure>

                    <div v-if="aboutAvada[i].title" class="title">
                        <h5>{{aboutAvada[i].title}}</h5>
                    </div>

                    <p class="description" v-if="aboutAvada[i].description">{{aboutAvada[i].description}}</p>

                    <button class="btn-learn-more" v-if="aboutAvada[i].button">{{aboutAvada[i].button}}</button>

                    <FooterTwit v-if="aboutAvada[i].twitImg" :twitImg="aboutAvada[i].twitImg"/>

                    <ul class="contacts-container" v-if="aboutAvada[i].contactList">
                        <li class="contact-wrapper" v-for="(element, j) in aboutAvada[i].contactList" :key="j">
                            <i class="contact-icon" :class="element.icon"></i>
                            <div class="contact-info" v-if="element.info">{{element.info}}</div>
                            <div class="contact-info-location" v-else>{{element.infoLocation}}</div>
                        </li>
                    </ul>

                    <figure class="location-wrapper" v-if="aboutAvada[i].image">
                        <img class="location" :src="aboutAvada[i].image" alt="">
                    </figure>
                </div>
            </div>
          </section>

          <section class="secondary-section">

          </section>
      </div>
  </footer>
</template>

<script>
import FooterTwit from './FooterTwit.vue';

export default {
    name: 'FooterAbout',
    components: {
      FooterTwit
    },

    data () {
      return {
        aboutAvada: [
          {
            logo: require ('../assets/images/footer-logo.png'),
            description: 'We are specialists in the construction of unique and exclusive properties. Our work inspires. We pride ourselves on delivering outstanding quality and design for leading clients across the world.',
            button: 'learn more',
          },
          {
            title: 'latest tweets',
            twitImg: require('../assets/images/En2TRxLW4AEiWUN.jpeg'),
          },
          {
            title: 'Contact us today',
            contactList: [
              {
                icon: 'fa-solid fa-globe',
                infoLocation: 'Corporate Location 1600 Amphitheatre Parkway London WC1 1BA'
              },
              {
                icon: 'fa-solid fa-house-chimney',
                infoLocation: 'Residential Location 9521 Broadsberry Avenue Paddington RC7 9ZA'
              },
              {
                icon: 'fa-solid fa-phone-flip',
                info: '1.800.458.556 / 1.800.532.2112'
              },
              {
                icon: 'fa-regular fa-envelope',
                info: 'info@your-domain.com'
              },
              {
                icon: 'fa-regular fa-clock',
                info: 'Monday – Friday: 9:00 AM – 6:00 PM'
              },
              {
                icon: 'fa-regular fa-clock',
                info: 'Saturday – Sunday: 9:00 AM – 12:00 PM'
              }
            ]
          },
          {
            title: 'find us',
            image: require ('../assets/images/construction_map_pin.png')
          }
        ],
      }
    }
}
</script>

<style lang="scss" scoped>

@import '../assets/scss/variables.scss';
@import '../assets/scss/mixins.scss';

.footer-container{
  position: relative;
  display: flex;
  flex-direction: column;
}

.main-section{
  background-color: #1E1E1E;
}

.container{
  margin: 0 auto;
  display: flex;
  gap: 3%;
  padding: 60px 0;
  width: 92%;

  .card{
      width: calc(91% / 4);
      margin-bottom: 10px;

      .logo-wrapper{
          padding-top: 10px;
          height: 70px;
          margin-bottom: 20px;

          img{
            height: 100%;
          }
      }

      .title{
          color: $light-color;
          text-transform: uppercase;
          margin-bottom: 20px;
      }

      .description{
          color: $gray-font;
          margin-bottom: 12px
      }

      .btn-learn-more{
        @include btn-light;
        font-size: 0.75rem;
        text-transform: uppercase;
        padding: 8px 25px;
      }

      .location-wrapper{
          .location{
              width: 250px;
          }
      }

      .contacts-container{
          .contact-wrapper{
              color: $gray-font;
              margin-bottom: 10px;
              font-size: 0.78rem;
              line-height: 1.30rem;
              display: flex;
              // width: 60%;

              .contact-icon{
                padding: 5px 10px 0 0;
              }

              .contact-info-location{
                width: 60%;
              }
              
          }
      }

  }
}

.secondary-section{
  flex-grow: 1;
  background-color: #121212;
}

</style>