<template>
  <footer>
      <div class="footer-container">
          <section class="main-section">
              <div class="main-container">
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
              <div class="secondary-container">
                  <div class="copyright-wrapper">
                      <div class="copyright">Copyright 2021-2022</div>
                      <div class="theme">Avada theme by <span>theme fusion</span></div>
                      <div class="rights">all rights reserved</div>
                      <div class="powered">powered by <span>me, myself and I</span></div>
                  </div>

                  <div class="social-media">
                    <a href="">
                      <i v-for="(icon, i) in socialMedia" :key="i" :class="icon"></i>
                    </a>
                  </div>
              </div>
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

        socialMedia:[
          'fab fa-facebook-f',
          'fab fa-twitter',
          'fab fa-youtube',
          'fab fa-instagram'
        ]
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

.main-container{
  margin: 0 auto;
  display: flex;
  gap: 3%;
  padding: 60px 0;
  width: 91%;

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
        border: none;
        font-size: 0.75rem;
        text-transform: uppercase;
        padding: 8px 25px;
      }

      .location-wrapper{
          .location{
              width: 95%;
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
  background-color: #121212;

  .secondary-container{
    color: #4d4d4d;
    display: flex;
    align-content: center;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 10px;
    width: 92%;
    margin: 0 auto;
    padding: 18px 0;

    .copyright-wrapper{
      display: flex;
      font-size: 0.6rem;

      div:nth-child(n+2){ //seleziono gli ultimi 3 div
        text-transform: uppercase;
      }

      .theme, .powered{
        span{
          color: dimgray;
        }
      }

      .rights{
        padding: 0 8px;
        border-right: 1px solid #4d4d4d;
        border-left: 1px solid #4d4d4d;
        margin: 0 8px;
      }
    }

    .social-media{
      .fab{
        margin: 0 8px;
        font-size: 0.8rem;
      }
    }
  }
}

@media screen and (min-width: 576px) and  (max-width: 992px){

  .main-container{
    flex-wrap: wrap;
    justify-content: center;

    .card{
      width: 45%;
    }
  }
}

@media screen and (max-width: 575px){
  .main-container{
    flex-wrap: wrap;
    justify-content: center;
    gap: 30px;

    .card{
      width: 100%;

      .location-wrapper{
        .location{
          width: 80%;
          display: block;
          margin: 0 auto;
        }
      }
    }

  }
}


</style>