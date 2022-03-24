<template>
    <header>
        <div class="header-container">
            <figure class="logo-wrapper">
                <img class="logo" src="../assets/images/construction_logo.png" alt="">
            </figure>

            <div class="navbar-container navbar-row">
                <ul class="navbar">
                    <!-- assegno la class active al primo elemento dell'array options  con :class="{'currentPage' : i === 0}-->
                    <li class="nav-option" v-for="(option, i) in options" :key="i" :class="{'currentPage' : i === 0}">
                        <a href="">{{option}}</a>
                    </li>
                    <button class="btn-quote">get quote</button>
                </ul>
                <a href="#" class="open" @click="click()" :class="{'hide' : this.clicked}">
                    <i class="fas fa-bars"></i>
                </a>
            </div>

            <div class="navbar-container navbar-hamburger" :class="{'open-hamburger' : this.clicked}">
                <ul class="navbar">
                    <!-- assegno la class active al primo elemento dell'array options  con :class="{'currentPage' : i === 0}-->
                    <li class="nav-option" v-for="(option, i) in options" :key="i" :class="{'currentPage' : i === 0}">
                        <a href="">{{option}}</a>
                    </li>
                    <button class="btn-quote">get quote</button>
                </ul>
                <a href="#" class="close" @click="click()" :class="{'hide' : !this.clicked}">
                    <i class="fas fa-times"></i>
                </a>
            </div>
        </div>
    </header>
</template>

<script>
export default {
    name: 'HeaderNavbar',
    data () {
        return {
            options: [
                'home',
                'about',
                'services',
                'work',
                'articles',
            ],

            clicked: false,
            index: 0,
        }
    },

    methods: {
        click: function () {
            if(this.index === 0){
                this.index++;
                this.clicked = true;
            }else{
                this.index--;
                this.clicked = false;
            }

            console.log('succede qualcosa', this.index, this.clicked)
        }
    }
}
</script>

<style lang="scss" scoped>

@import '../assets/scss/variables.scss';
@import '../assets/scss/mixins.scss';

header{
    width: 100%;
    font-size: 0.875rem;
    position: sticky;
    top: 0;
    z-index: 10;
    background-color: white;
}

.header-container{
    // padding: 18px 0;
    max-width: 91%;
    margin: 0 auto;
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: wrap;

    .logo-wrapper{
        padding: 10px 20px 10px 0;

        .logo{
            width: 165px;
        }
    }

    .navbar-container{

        .navbar{
            color: $gray-font;
            font-size: 0.7rem;
            text-transform: uppercase;
            display: flex;
            align-items: center;
            flex-wrap: wrap;
            gap: 30px;
    
            .btn-quote{
                @include btn-common;
                padding: 12px 25px;
                @include btn-light;
                color: $gray-font;
            }
    
            .currentPage{
                color: $light-color;
    
                &::after{
                    content: '';
                    position: absolute;
                    top: 100%;
                    left: 50%;
                    transform: translate(-50%);
                    border-style: solid;
                    border-width: 10px 10px 0 10px;
                    border-color: white transparent transparent transparent;
                }
            }
        }
    }

    .nav-option{ //l'ho messo qui cosí é piú facile togliere il padding nelle media queery
        position: relative;
        padding: 38px 0;

        a:hover{
            color: $light-color;
        }
    }

    .navbar-row{
        .open{
            display: none;
            font-size: 2rem;
            color: $light-color;

            &:hover{
                color: $dark-color;
            }
        }
    }

    .navbar-hamburger{
        display: none;
        
        .navbar{
            position: absolute;
            top: 80px;
            left: 0;
            width: 100%;
            display: flex;
            flex-direction: column;
            background-color: white;
        }

        .close{
            position: absolute;
            top: 21px;
            right: 31px;
            font-size: 2rem;
            color: $light-color;
        }
    }

    .open-hamburger{ // classe che assegno a navbar-hambuer per mostrarlo
        display: block;
    }

}

@media screen and (max-width: 768px){
    .header-container{
        .navbar-row{

            .navbar{
                display: none;
            }

            .open{
                display: block;
            }

            .hide{
                display: none;
            }
        }

        //--------------------

        .navbar-hamburger{

            .navbar{
                padding: 20px;

                .nav-option{
                    padding: 0;
                    font-size: 1rem;
                }
            }
        }

    }
}


@media screen and (max-width: 575px){

    .header-container{
        gap: 25px;

        .navbar{
            padding-bottom: 25px;

            .nav-option{
                padding: 0;
            }
    
            .currentPage::after{
                display: none;
            }
        }
    }

}


</style>