<template>
    <a-layout class="outer-wrapper">
        <a-layout-content class="wrapper">
            <TwoColumnLayout bgText="START-UPS">
                <template v-slot:text>
                    <h2 v-scroll-reveal>Tech Start-ups</h2>
                    <div class="separator"></div>
                    <h3 v-scroll-reveal>Let’s Scale-Up the Market</h3>
                    <p v-scroll-reveal>One of my latest investment projects introduced me to the enormous potential, vast expertise, and encouraging business environment of the tech industry. The potential immediately hooked me. Thus, I decided to start investing in it and helping ambitious tech-startups scale up from local to international markets.</p>
                </template>
                <template v-slot:image>
                    <picture v-scroll-reveal>
                        <source media="(min-width: 1024px)" srcset="~@/assets/images/TStart_ups_desk.jpg 1x, ~@/assets/images/TStart_ups_desk@2x.jpg 2x" />
                        <source media="(min-width: 768px)" srcset="~@/assets/images/TStart_ups_tab.jpg 1x, ~@/assets/images/TStart_ups_tab@2x.jpg 2x">
                        <source media="(min-width: 360px)" srcset="~@/assets/images/TStart_ups_mob.jpg 1x, ~@/assets/images/TStart_ups_mob@2x.jpg 2x">
                        <img src="~@/assets/images/TStart_ups_desk.jpg" alt="Hands expression an idea" />
                    </picture>
                </template>
            </TwoColumnLayout>
            <TwoColumnLayout :flip="true">
                <template v-slot:text>
                    <h2 v-scroll-reveal>Investment requirements</h2>
                    <div class="separator"></div>
                    <p v-scroll-reveal>I believe in and am looking for start-ups that are in their post-accelerator period, have knowledge about their market, a strategy to penetrate it, and an adequate financial plan in hand. To know more about my investment criteria, please go through the requirements below.</p>
                </template>
                <template v-slot:image>
                    <picture v-scroll-reveal>
                        <source media="(min-width: 1024px)" srcset="~@/assets/images/IRequirements_desk.jpg 1x, ~@/assets/images/IRequirements_desk@2x.jpg 2x" />
                        <source media="(min-width: 768px)" srcset="~@/assets/images/IRequirements_tab.jpg 1x, ~@/assets/images/IRequirements_tab@2x.jpg 2x">
                        <source media="(min-width: 360px)" srcset="~@/assets/images/IRequirements_mob.jpg 1x, ~@/assets/images/IRequirements_mob@2x.jpg 2x">
                        <img src="~@/assets/images/IRequirements_desk.jpg" alt="People around a table using digital devices" />
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
        background-color: transparent;
        position: relative;
        padding: 210px 0 0px;
        @media screen and (max-width: $media-tablet) {
            padding: 150px 0 0px;
        }
        @media screen and (max-width: $media-mobile) {
            padding: 60px 0 0px;
        }
        .wrapper{
            column-gap: 150px;
            &:not(:last-child){
                margin-bottom: 150px;
                @media screen and (max-width: $media-tablet) {
                    margin-bottom: 60px;
                }
            }
        }
    }
    
</style>
