<template>
    <div class="faq grid" 
        @click="handleClick(index)" 
        v-bind:class="{ active: activeIndex === index }">
        <div class="icon-buttons">
            <a-button type="primary" shape="circle" class="icon-btn plus" icon="plus" size="large" v-if="activeIndex !== index" />
            <a-button type="primary" shape="circle" class="icon-btn" icon="minus" size="large" v-if="activeIndex === index" />
        </div>
        <div class="text">
            <h5 class="text-light">{{title}}</h5>
            <div v-show-slide="activeIndex === index">
                <slot></slot>
            </div>
        </div>
    </div>
</template>

<script>

export default {
    components: {
    },
    props: {
        index: Number,
        title: String,
        activeIndex: Number
    },
    methods: {
        handleClick (number) {
            this.$emit('toggleFeatures', number);
            
        }
    }
}
</script>

<style scoped lang="scss">
    .icon-btn{
        background-color: #FFFFFF;
        color: $brand-color;
        -webkit-transition: all 0.3s ease-in-out;
        -moz-transition: all 0.3s ease-in-out;
        -ms-transition: all 0.3s ease-in-out;
        -o-transition: all 0.3s ease-in-out;
        transition: all 0.3s ease-in-out;
        i{
            position: relative;
            top: -1px;
        }
        &.plus{
            background-color: $brand-color;
            color: #FFFFFF;
            border: 3px solid #FFFFFF;
        }
    }

    .faq{
        display: grid;
        max-width: 800px;
        margin-bottom: 30px;
        cursor: pointer;
        grid-template-columns: 60px 1fr;
        align-items: baseline;
        //padding: 25px 100px 0px 40px;
        @media screen and (max-width: $media-tablet) {
            
        }
        @media screen and (max-width: $media-mobile) {
            
        }
        p,h5{
            margin: 0;
            white-space: pre-wrap;
        }
      
    }
</style>
