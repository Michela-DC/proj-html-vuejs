<template>
    <header>
        <div class="header-container">
            <figure class="logo-wrapper">
                <img class="logo" src="../assets/images/construction_logo.png" alt="">
            </figure>

            <ul class="navbar">
                <li class="nav-option" v-for="(option, i) in options" :key="i">{{option}}</li>
                <button class="btn-quote">get quote</button>
            </ul>
        </div>
    </header>
</template>

<script>
export default {
    name: 'MainHeader',
    data () {
        return {
            options: [
                'home',
                'about',
                'services',
                'work',
                'articles',
            ]
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
    // min-height: 88px;
    // max-width: 1254px;
    padding: 18px 0;
    max-width: 87%;
    margin: 0 auto;
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: wrap;

    .logo-wrapper{
        .logo{
            width: 145px;
        }
    }

    .navbar{
        text-transform: uppercase;
        display: flex;
        align-items: center;
        flex-wrap: wrap;
        gap: 25px;

        .btn-quote{
            // padding: 10px 25px;
            @include btn-common;
            @include btn-light;
        }
    }
}


</style>