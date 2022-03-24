<template>
    <header>
        <div class="header-container">
            <figure class="logo-wrapper">
                <img class="logo" src="../assets/images/construction_logo.png" alt="">
            </figure>

            <ul class="navbar">
                <!-- assegno la class active al primo elemento dell'array options  con :class="{'active' : i === 0}-->
                <li class="nav-option" v-for="(option, i) in options" :key="i" :class="{'active' : i === 0}">{{option}}</li>
                <button class="btn-quote">get quote</button>
            </ul>
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
        }
    },

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
        .logo{
            width: 165px;
        }
    }

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

        .nav-option{
            position: relative;
            display: block;
            height: 100%;
            padding: 38px 0;
            
        }

        .active{
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


</style>