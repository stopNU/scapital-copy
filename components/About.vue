<template>
    <a-layout class="outer-wrapper">
        <div class="top-curv-bar"></div>
        <a-layout-content class="wrapper">
            <TwoColumnLayout bgText="About">
                <template v-slot:text>
                    <h2 v-scroll-reveal>A Small Introduction from Me</h2>
                    <div class="separator"></div>
                    <p v-scroll-reveal>
                        I started my career as a sales manager in the real estate industry. There I managed large portfolios in vastly competitive markets such as the Netherlands, Hong Kong, and Switzerland. However, my passion for the financial world had soon taken me on the path of becoming a full-time, self-supporting business investor. 
                        <br><br>
                        Since then, I have gained a solid background in numerous business initiatives around the world. I manage two investment groups in the Netherlands and take an active part in wealth management programs at Credit Suisse. Also, I manage to feed my hunger for traveling and experiencing different cuisines with business trips to the UAE and Asia markets as a real estate consultant. 
                        <br><br>
                        The little free time I have, I spent with my family, cooking, playing sports with the kids, or capturing glimpses of the universe through the lenses of my camera.
                    </p>
                </template>
                <template v-slot:image>
                    <picture v-scroll-reveal>
                        <source media="(min-width: 1024px)" srcset="~@/assets/images/stephan_desk.jpg 1x, ~@/assets/images/stephan_desk@2x.jpg 2x" />
                        <source media="(min-width: 768px)" srcset="~@/assets/images/stephan_tab.jpg 1x, ~@/assets/images/stephan_tab@2x.jpg 2x">
                        <source media="(min-width: 360px)" srcset="~@/assets/images/stephan_mob.jpg 1x, ~@/assets/images/stephan_mob@2x.jpg 2x">
                        <img src="~@/assets/images/stephan_desk.jpg" alt="Stepan portrait with sunglasses" />
                    </picture>
                </template>
            </TwoColumnLayout>
        </a-layout-content>
    </a-layout>
</template>

<script>
import TwoColumnLayout from '~/components/shared/TwoColumnLayout.vue'

export default {
    components: {
        TwoColumnLayout
    },
}
</script>

<style scoped lang="scss">
    .outer-wrapper{
        background-color: #FFFFFF;
        position: relative;
        padding: 180px 0 150px;
        @media screen and (max-width: $media-tablet) {
            padding: 150px 0 120px;
        }
        @media screen and (max-width: $media-mobile) {
            padding: 60px 0;
        }
    }
    .top-curv-bar{
        background-color: #FFFFFF;
    }
</style>
