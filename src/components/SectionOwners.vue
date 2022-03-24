<template>
  <section class="section-owners">
      <div class="container">
            <div class="row">
                <h3 class="title">Our home owners say</h3>

                <div class="slide" v-for="(slide, i) in slides" :key="i" :class="activeSlide(i)">
                    <figure class="owner-img">
                        <img class="owner-photo" :src="slide.ownerPhoto" alt="">
                    </figure>

                    <p class="owner-says">
                        " {{slide.ownerSays}} "
                    </p>

                    <div class="owner-name">
                        <div class="name">{{slide.ownerName}}</div>
                        <div class="role">new home owner</div>
                    </div>

                    <div class="btn-wrapper">
                        <!-- assegno la classe active-btn al primo bottone se l'indice é uguale a 0 -->
                        <button class="radio-button" @click="first()" :class="{'active-btn' : i === 0}"></button>
                        <!-- assegno la classe active-btn al primo bottone se l'indice é uguale a 1 -->
                        <button class="radio-button" @click="second()" :class="{'active-btn' : i === 1}"></button>
                    </div>
                </div>
            </div>
      </div>
  </section>
</template>

<script>
export default {
    name: 'SectionOwners',

    data () {
        return{
            slides: [
                {
                    ownerPhoto: require("../assets/images/home-testimonial-113165296.jpg"),
                    ownerSays: "No man but feels more of a man in the world if he have but a bit of ground that he can call his own. However small it is on the surface, it is four thousand miles deep; and that is a very handsome property.",
                    ownerName: "Jane Smith"
                },
                {
                    ownerPhoto: require("../assets/images/home-testimonial-84268399.jpg"),
                    ownerSays: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Distinctio corporis commodi accusantium dolore, possimus itaque repellat quaerat esse sed expedita velit deleniti quam in? Quidem.",
                    ownerName: "John Doe"
                }
            ],

            activeIndex: 0,
            clock: undefined,
        }
    },

    methods: {

        activeSlide: function (index){
            if(this.activeIndex === index){
                return 'activeSlide';
            }
        },

        next: function () {
            // potevo anche solo usare this.activeIndex = 1  dato che ho solo due slide ma in questo modo se aggiungo altre slide il loop continua in ordine 
            if (this.activeIndex < this.slides.length - 1){ 
            // se l'indice è minore della lunghezza dell'array - 1 (ovvero minore delle posibili posizione dentro l'array allora incremento l'indice
                this.activeIndex ++;
            } else{
            // se l'indice diventa maggiore della lunghezza dell'array - 1 allora lo faccio ritornare a zero, ovvero alla posizione della prima immagine nell'array
                this.activeIndex = 0;
            }
            
        },

        previous: function () {
            if ( this.activeIndex > 0){ 
            //decremento l'activeIndex per stabilire la nuova slide corrente
                this.activeIndex --;

            } else {
                // potevo anche solo usare this.activeIndex = 1 ma in questo modo se aggiungo altra slide quando sono all'ultima slide ritorna alla prima
                this.activeIndex = this.slides.length - 1;
            } 
            
        },

        first: function() {
            // quando clicco sul primo bottone l'indice va a 0 quindi sono alla prima immagine
            this.activeIndex = 0;
        },

        second: function() {
            // quando clicco sul primo bottone l'indice va a 1 quindi sono alla 2' immagine
            this.activeIndex = 1;
        },

        startAutoplay: function (){
            this.clock = setInterval (this.next, 4000);
        },
    },

    mounted() {
        this.startAutoplay();
    },
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
}

.row{
    @include small-row;
    color: white;
    display: flex;
    align-items: center;
    flex-direction: column;
    gap: 25px;

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

    .slide{
        gap: 25px;
        // display: flex;
        display: none;
        align-items: center;
        flex-direction: column;
        text-align: center;
    
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

        .btn-wrapper{
        .radio-button{
            width: 12px;
            height: 12px;
            border-radius: 50%;
            border: 1px solid white;
            margin: 5px;
            background-color: transparent;
        }

        .active-btn{
            background-color: white;
        }
    }
    }

    .activeSlide{
        display: flex;
    }
}

</style>