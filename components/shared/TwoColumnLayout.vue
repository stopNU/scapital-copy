<template>
    <div class="wrapper" v-bind:class="{ flip: flip }">
            <span v-if="bgText" class="background-text">{{bgText}}</span>
            <div class="text-wrapper">
                <slot name="text">Title</slot>
            </div>
            <div class="image-wrapper">
                <slot name="image">Title</slot>
            </div>
           
      </div>
</template>

<script>
export default {
    components: {
    },
    props: {
        bgText: String,
        flip: Boolean
    }
}
</script>

<style scoped lang="scss">
    .background-text{
        position: absolute;
        top: 138px;
        @media screen and (max-width: $media-tablet) {
            top: 105px;
        }
        @media screen and (max-width: $media-mobile) {
            top: 15px;
        }
    }
   .wrapper{
        display: grid;
        grid-template-areas: 'text image';
        align-items: center;
        column-gap: 60px;
        overflow: hidden;
        &.flip{
            grid-template-areas: 'image text';
        }
        @media screen and (max-width: $media-tablet-xl) {
            row-gap: 60px;
            grid-template-areas: 
            'text'
            'image';
            &.flip{
                grid-template-areas: 
                'text'
                'image';
            }
        }
        @media screen and (max-width: $media-mobile) {
            row-gap: 30px;
        }
   }
    
    .text-wrapper{
        grid-area: text;
        h2{
            max-width: 600px;
            @media screen and (max-width: $media-mobile) {
                margin-bottom: 15px;
            }
        }
        .separator{
            margin-bottom: 30px;
            @media screen and (max-width: $media-mobile) {
                margin-bottom: 20px;
            }
        }
        @media screen and (max-width: $media-tablet) {
            p{
                max-width: 600px;
            }
        }
    }
    .image-wrapper{
        grid-area: image;
        max-width: 700px;
        z-index: 1;
        position: relative;
        @media screen and (max-width: $media-tablet) {
            max-width: 100%;
            img{
                width: 100%;
            }
        }
    }
</style>
