<template>
    <div class="info">
        <div>
            <h5 class="text-brand" v-scroll-reveal>Phone:</h5>
            <h6 v-scroll-reveal>+31652480941</h6>
        </div>
        <div>
            <h5 class="text-brand" v-scroll-reveal>Email:</h5>
            <h6 v-scroll-reveal>s.akerboom@ogmaatschapfabo.nl</h6>
        </div>
        <div>
            <h5 class="text-brand" v-scroll-reveal>Address:</h5>
            <h6 v-scroll-reveal>Residenza La Fiorita,<br>
                Via Ruvigliana 23,<br>
                6962 Lugano Viganello (Swiss)</h6>
        </div>
        <div class="social-media">
            <h5 v-scroll-reveal class="text-brand">social media</h5>
            <a href="https://linkedin.com/in/stephan-akerboom-65009b25" target="_blank" v-scroll-reveal><img class="linkedin" src="~@/assets/icons/linkedin.svg" alt="LinkedIn"></a>
        </div>
    </div>  
</template>

<style scoped lang="scss">
    .info{
        margin-top: 60px;
        @media screen and (max-width: $media-tablet) {
            display: grid;
            grid-template-columns: 1fr 1fr;
            margin-top: 0px;
        }
        div{
            margin-bottom: 30px;
            h5{
                margin-bottom: 15px;
                @media screen and (max-width: $media-mobile) {
                    margin-bottom: 0px;
                }
            }
        }
    }
    .social-media{
        img{
            cursor: pointer;
            &:hover{
                opacity: 0.7;
            }
        }
    }
    
    .mobile{
        .info{
            grid-template-columns: 1fr;
            div{
                margin-bottom: 20px;
            }
            h5, h6{
                color: $text-color-dark;
                @media screen and (max-width: $media-mobile) {
                       
                }
            }
            @media screen and (max-width: $media-mobile) {
                h5{
                    font-size: 17px;
                    font-weight: 600; 
                    line-height: 25.5px;
                }
                h6{
                    font-size: 12px;
                }
            }
        }
    }
</style>
