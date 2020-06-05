<template>
    <a-layout class="outer-wrapper">
        <a-layout-content class="wrapper">
            <div class="intro">
                <h3 class="text-light" v-scroll-reveal>My Business Philosophy</h3>
                <div class="separator white"></div>
                <p class="text-light" v-scroll-reveal>
                    Stepping on substantial experience and using a vast network of connections to implement a clear and shared business vision is what makes me a good business partner.
                </p>
            </div>
            <div class="boxes">
                <div class="box">
                    <div class="icon">
                        <img src="~@/assets/icons/experience_ic.svg" alt="Experience" v-scroll-reveal>
                    </div>
                    <h5 class="text-light" v-scroll-reveal>Experience</h5>
                    <p class="text-light" v-scroll-reveal>I have a solid background in the business world, with tens of successful projects behind my back and strong financial expertise.</p>
                </div>
                <div class="box">
                    <div class="icon">
                        <img src="~@/assets/icons/connections_ic.svg" alt="Connections" v-scroll-reveal>
                    </div>
                    <h5 class="text-light" v-scroll-reveal>Connections</h5>
                    <p class="text-light" v-scroll-reveal>Throughout my business ventures, I established numerous business relationships around Europe and Asia, which benefit the tech start-ups I invest in.</p>
                </div>
                <div class="box">
                    <div class="icon">
                        <img src="~@/assets/icons/vision_ic.svg" alt="Vision" v-scroll-reveal>
                    </div>
                    <h5 class="text-light" v-scroll-reveal>Vision</h5>
                    <p class="text-light" v-scroll-reveal>Establishing a clear and robust vision, shared across all stakeholders is what makes my business ventures successful in the long run.</p>
                </div>
            </div>
        </a-layout-content>
    </a-layout>
</template>

<script>
export default {

}
</script>

<style scoped lang="scss">
    .boxes{
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        column-gap: 30px;
        text-align: center;
        @media screen and (max-width: $media-tablet) {
            grid-template-columns: repeat(1, 1fr);
            max-width: 500px;
            margin: 0 auto;
            row-gap: 60px;
        }
        .box{
            h5{
                margin-top: 30px;
            }
            p{
                padding: 0 10px;
            }
        }
    }
    .outer-wrapper{
        background-color: transparent;
        .wrapper{
            padding: 150px 0 250px; 
            @media screen and (max-width: $media-tablet) {
                padding: 150px 0 100px; 
                padding: 0 $side-padding-tablet;
            }
            @media screen and (max-width: $media-mobile) {
                padding: 60px 0; 
                max-width: 350px;
                margin-bottom: 60px;
                h5{
                    margin-bottom: 10px;
                }
            }
        }
    }
    .intro{
        text-align: center;
        max-width: 520px;
        margin: 0 auto 60px;
        .separator{
            margin: 0 auto 30px;
        }
    }
</style>
