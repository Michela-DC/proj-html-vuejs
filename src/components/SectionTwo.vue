<template>
    <section class="section-2">
        <div class="question-container">
            <div class="question-row">
                <h2>Do you have a construction project we can help with?</h2>
                <button>get a free quote</button>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'SectionTwo'
}
</script>

<style lang="scss" scoped>

@import '../assets/scss/mixins.scss';
@import '../assets/scss/variables.scss';

.question-container{
    background-color: $light-color;

    .question-row{
        @include small-row;
        margin: 0 auto;
        min-height: 130px;
        display: flex;
        justify-content: center;
        position: relative;
        padding-top: 45px;
        
        button{
            @include btn-dark;
            @include btn-common;
            // padding: 10px 25px;
            text-transform: uppercase;
            border: 2px solid white;
            font-size: 0.875rem;
            position: absolute;
            top: 80%;
            left: 50%;
            transform: translate(-50%);
        }
    }

}

</style>