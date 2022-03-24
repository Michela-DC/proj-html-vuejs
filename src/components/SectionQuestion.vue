<template>
    <section class="section-question">
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
    name: 'SectionQuestion'
}
</script>

<style lang="scss" scoped>

@import '../assets/scss/mixins.scss';
@import '../assets/scss/variables.scss';

.section-question{
    background-color: $light-color;
}

.question-container{
    padding: 20px;

    .question-row{
        // min-height: 130px;
        display: flex;
        justify-content: center;
        position: relative;
        padding: 20px 0 30px 0;
        margin: 0 auto;

        button{
            background-color: $dark-color;
            color: $light-gray;
            @include btn-common;
            text-transform: uppercase;
            border: 2px solid white;
            font-size: 0.80rem;
            position: absolute;
            top: 96%;

            &:hover{
                background-color: white;
                border: 2px solid $dark-color;
                color: $dark-color;
            }
        }
        
    }

}

</style>