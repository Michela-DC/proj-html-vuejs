<template>
    <div class="twit-container">
        <div class="twit-content">
            <div class="account-logo-wrapper">
                <img class="account-logo" src="../assets/images/3a74ce3d0532b7773b174c45ca3bd05a_normal.png" alt="">
            </div>

            <svg class="twitter-icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 72 72"><path fill="none" d="M0 0h72v72H0z"/><path class="icon" fill="#667580" d="M68.812 15.14c-2.348 1.04-4.87 1.744-7.52 2.06 2.704-1.62 4.78-4.186 5.757-7.243-2.53 1.5-5.33 2.592-8.314 3.176C56.35 10.59 52.948 9 49.182 9c-7.23 0-13.092 5.86-13.092 13.093 0 1.026.118 2.02.338 2.98C25.543 24.527 15.9 19.318 9.44 11.396c-1.125 1.936-1.77 4.184-1.77 6.58 0 4.543 2.312 8.552 5.824 10.9-2.146-.07-4.165-.658-5.93-1.64-.002.056-.002.11-.002.163 0 6.345 4.513 11.638 10.504 12.84-1.1.298-2.256.457-3.45.457-.845 0-1.666-.078-2.464-.23 1.667 5.2 6.5 8.985 12.23 9.09-4.482 3.51-10.13 5.605-16.26 5.605-1.055 0-2.096-.06-3.122-.184 5.794 3.717 12.676 5.882 20.067 5.882 24.083 0 37.25-19.95 37.25-37.25 0-.565-.013-1.133-.038-1.693 2.558-1.847 4.778-4.15 6.532-6.774z"/></svg>
            
            <div class="account">ThemeFusion</div>
            <div class="account-id">@Theme_Fusion</div>

            <p class="twit-text">
                Lorem, ipsum dolor sit amet consectetur adipisicing elit. Aperiam facilis, nobis reprehenderit numquam sapiente animi in at fugiat cumque architecto tempore ipsam. Voluptas, est sapiente. 
                <span>#avadaconstruction</span>
            </p>
            
            <figure class="twit-img-wrapper">
                <img :src="twitImg" alt="">
            </figure>

            <div class="bottom-svg">
                <svg class="heart" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path class="icon" fill="#667580" d="M12 21.638h-.014C9.403 21.59 1.95 14.856 1.95 8.478c0-3.064 2.525-5.754 5.403-5.754 2.29 0 3.83 1.58 4.646 2.73.813-1.148 2.353-2.73 4.644-2.73 2.88 0 5.404 2.69 5.404 5.755 0 6.375-7.454 13.11-10.037 13.156H12zM7.354 4.225c-2.08 0-3.903 1.988-3.903 4.255 0 5.74 7.035 11.596 8.55 11.658 1.52-.062 8.55-5.917 8.55-11.658 0-2.267-1.822-4.255-3.902-4.255-2.528 0-3.94 2.936-3.952 2.965-.23.562-1.156.562-1.387 0-.015-.03-1.426-2.965-3.955-2.965z"/></svg>
                <svg class="exit" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path class="icon" fill="#667580" d="M21.78 11.47l-5.14-5.14c-.292-.292-.767-.292-1.06 0s-.293.77 0 1.062l3.858 3.858H8.918c-.415 0-.75.336-.75.75s.335.75.75.75h10.52l-3.857 3.858c-.29.293-.29.768 0 1.06.148.147.34.22.53.22s.386-.072.53-.22l5.14-5.138c.294-.293.294-.767 0-1.06z"/><path class="icon" fill="#667580" d="M9.944 20.5H4.292c-.437 0-.792-.355-.792-.792V4.292c0-.437.355-.792.792-.792h5.652c.414 0 .75-.336.75-.75S10.358 2 9.944 2H4.292C3.028 2 2 3.028 2 4.292v15.416C2 20.972 3.028 22 4.292 22h5.652c.414 0 .75-.336.75-.75s-.336-.75-.75-.75z"/></svg>  
                <span class="hour">22h</span>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'FooterTwit',
    props: [
        'twitImg',
    ]

}
</script>

<style lang="scss" scoped>

@import '../assets/scss/variables.scss';
@import '../assets/scss/mixins.scss';

.twit-container{
    color: white;
    display: flex;
    flex-direction: column;
    align-items: flex-end;

    padding-top: 10px;

    .twit-content{
        width: 80%;
        font-size: 0.78rem;
        position: relative;

        .account-logo-wrapper{
            border: 1px solid green;
            position: absolute;
            top: 0;
            // right: 100%;
            left: -37px;
            border-radius: 50%;
            overflow: hidden;
            height: 30px;
            width: 30px;

            .account-logo{
                width: 100%;
            }
        }

        .twitter-icon{
            width: 16px;
            position: absolute;
            right: 0;
            top: 0px;
        }

        .account{
            font-weight: bold;
        }

        .account-id{
            color: $gray-font;
        }

        .twit-text{
            line-height: 1rem;
            margin-bottom: 20px;

            span{
                color: #1E90FF;
            }
        }

        .twit-img-wrapper{
            width: 100%;
            margin-bottom: 5px;

            img{
            width: 100%;
            display: block;
            }
        }

        .bottom-svg{
            position: relative;

            svg{
                width: 16px;
            }

            .heart{
                margin-right: 20px;
            }

            .hour{
                position: absolute;
                right: 0;
                color: $gray-font;
            }
        }
    }

}

</style>