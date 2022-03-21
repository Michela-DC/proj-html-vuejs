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

header{
    width: 100%;
    font-size: 15px;
}

.header-container{
    min-height: 68px;
    // max-width: 1254px;
    max-width: 87%;
    margin: 0 auto;
    display: flex;
    align-items: center;
    justify-content: space-between;

    .logo-wrapper{
        .logo{
            width: 120px;
        }
    }

    .navbar{
        text-transform: uppercase;
        display: flex;
        align-items: center;
        gap: 25px;

        .btn-quote{
            width: 120px;
            height: 38px;
            text-transform: uppercase;
            background-color: #fed23f;
            border: none;
        }
    }
}


</style>