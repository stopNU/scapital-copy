<template>
    <a-layout class="outer-wrapper">
        <a-layout-content class="wrapper">
            <div class="faqs">
                <h3 class="text-light" v-scroll-reveal>Investment checklist</h3>
                <div class="list" v-scroll-reveal>
                    <ChecklistItem :index="1" title="Management Team" @toggleFeatures="toggleFeatures" :activeIndex="activeIndex">
                        <ul>
                            <li><p>Proven track record of leading successful projects</p></li>
                            <li><p>High proactivity and inspiring business commitment</p></li>
                            <li><p>Openness to receiving advice and feedback from angel investors</p></li>
                        </ul>
                    </ChecklistItem>
                    <ChecklistItem :index="2" title="Market Opportunity" @toggleFeatures="toggleFeatures" :activeIndex="activeIndex">
                        <ul>
                            <li><p>Unique or highly competitive product/service</p></li>
                            <li><p>Identified market segment with proven demand</p></li>
                            <li><p>Projected large and growing spending in the service/product category</p></li>
                        </ul>
                    </ChecklistItem>
                    <ChecklistItem :index="3" title="Go-to-Market Strategy" @toggleFeatures="toggleFeatures" :activeIndex="activeIndex">
                        <ul>
                            <li><p>Clear and structured Business Model</p></li>
                            <li><p>Strategy to penetrate the market</p></li>
                        </ul>
                    </ChecklistItem>
                    <ChecklistItem :index="4" title="Financials" @toggleFeatures="toggleFeatures" :activeIndex="activeIndex">
                        <ul>
                            <li><p>Logical revenue plans based on market state</p></li>
                            <li><p>Financial plan taking in mind revenue shortfalls </p></li>
                            <li><p>Adequate gross margins and cash positions</p></li>
                        </ul>
                    </ChecklistItem>
                    <ChecklistItem :index="5" title="Proceeds Usage" @toggleFeatures="toggleFeatures" :activeIndex="activeIndex">
                        <ul>
                            <li><p>To expedite key goals and milestones</p></li>
                            <li><p>To increase the company’s market value</p></li>
                            <li><p>To strengthen market positioning or capture an analyzed opportunity</p></li>
                        </ul>
                    </ChecklistItem>
                    <ChecklistItem :index="6" title="Growth Potential" @toggleFeatures="toggleFeatures" :activeIndex="activeIndex">
                        <ul>
                            <li><p>Readiness to scale up</p></li>
                            <li><p>Growth plan</p></li>
                        </ul>
                    </ChecklistItem>
                    <ChecklistItem :index="7" title="Competition" @toggleFeatures="toggleFeatures" :activeIndex="activeIndex">
                        <ul>
                            <li><p>Identified market competitors</p></li>
                            <li><p>Analyzed entry barriers</p></li>
                            <li><p>Differentiation strategy – competitive advantage </p></li>
                        </ul>
                    </ChecklistItem>
                    <ChecklistItem :index="8" title="Technology" @toggleFeatures="toggleFeatures" :activeIndex="activeIndex">
                        <ul>
                            <li><p>First-to-market ideas are prioritized over improvements of standard products/services</p></li>
                            <li><p>I’m interested only in technologies with commercialization capacity</p></li>
                        </ul>
                    </ChecklistItem>
                    <ChecklistItem :index="9" title="Exit Strategy" @toggleFeatures="toggleFeatures" :activeIndex="activeIndex">
                        <ul>
                            <li><p>I seek high return on investment, due to the high risk of failure in early-stage ventures</p></li>
                            <li><p>Realistic exit strategy – how will you, me, and other investors extract financial gains</p></li>
                            <li><p>Operational strategy, involving specific steps to achieve exit</p></li>
                        </ul>
                    </ChecklistItem>
                </div>
            </div>
        </a-layout-content>
    </a-layout>
</template>

<script>
import ChecklistItem from '~/components/ChecklistItem.vue'

export default {
    components: {
        ChecklistItem
    },
    data () {
        return {
            activeIndex: null
        }
    },
    methods: {
        toggleFeatures (number) {
            if(this.activeIndex === number){
                this.activeIndex = null;
            }
            else{
                this.activeIndex = number;
            };

        }
    }
}
</script>

<style scoped lang="scss">
    .list{
        display: grid;
        grid-template-columns: 1fr 1fr;
        @media screen and (max-width: $media-tablet) {
            grid-template-columns: 1fr;
        }
    }
    .faqs{
        max-width: 1000px;
        box-shadow: 0px 3px 86px #00000042;
        margin: 0px auto 0;
        padding: 60px 120px;
        border-top-left-radius: 60px;
        border-bottom-right-radius: 60px;
        background-color: $brand-color;
        @media screen and (max-width: $media-mobile) {
            padding: 60px 15px;
        }
        h3{
            margin-bottom:60px;
        }
        ul{
            margin-left: -20px;
            color: #FFFFFF;
            li p{
                color: #FFFFFF;
            }
        }
    }
    .outer-wrapper{
        background-color: #FFFFFF;
        background-image: -webkit-horizontal-gradient(#F3F3F3 0%, #F3F3F3 50%, #FFFFFF 50%, #FFFFFF 50%);
        background-image: linear-gradient(#F3F3F3 0%, #F3F3F3 50%, #FFFFFF 50%, #FFFFFF 50%);
        padding: 150px 0;
        @media screen and (max-width: $media-tablet) {
            padding: 60px 0;
        }
        .wrapper{
            @media screen and (max-width: $media-mobile) {
                padding: 0;
            }
        }
    }
</style>
