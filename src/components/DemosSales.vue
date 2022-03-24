<template>
    <div class="demos-sale">
        <div class="demos">
            <div class="icon">
                <i class="fa-solid fa-folder-open"></i>
            </div>
            <div>Demos</div>
        </div>
        <div class="on-sale">
            <div class="sale-price">
                <span class="dollar">$</span>
                <span class="number">39</span>
            </div>
            <div>On Sale</div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'DemosSales'
}
</script>

<style lang="scss" scoped>

@import '../assets/scss/variables.scss';

.demos-sale{
    position: fixed;
    z-index: 20;
    top: 100px;
    right: 16px;

    .demos, .on-sale{
        background-color: white;
        width: 50px;
        height: 50px;
        border-radius: 5px;
        font-size: 0.625rem;
        text-align: center;
        display: flex;
        flex-direction: column;
        justify-content: center;
        font-weight: bold;
        box-shadow: 0px 0px 15px $gray-font;
    }

    .demos{
        margin-bottom: 5px;

        .icon{
            font-size: 1rem;
        }
    }

    .on-sale{
        .sale-price{
            font-size: 1.125rem;
            color: #53aa53;
            position: relative;
            margin-bottom: 3px;
            

            .dollar{
                position: absolute;
                top: 3px;
                font-size: 0.75rem;
            }

            .number{
                margin-left: 7px;
            }
        }
    }
}

@media screen and (max-width: 575px) {
    .demos-sale{
        display: none;
    }
}
</style>