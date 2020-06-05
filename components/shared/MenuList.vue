<template>
    <scrollactive :offset="100">
        <ul>
            <li @click="handleClick"><a href="#home" class="scrollactive-item">Home</a></li>
            <li @click="handleClick"><a href="#about-me" class="scrollactive-item">About me</a></li>
            <li @click="handleClick"><a href="#entrepreneurs" class="scrollactive-item">Entrepreneurs</a></li>
            <li @click="handleClick"><a href="#projects" class="scrollactive-item">Projects</a></li>
            <li @click="handleClick"><a href="#contacts" class="scrollactive-item">Contacts</a></li>
        </ul>
    </scrollactive>
</template>

<script>

export default {
    props:{
        mobile: Boolean,
    },
    methods:{
        handleClick(){
            if(this.mobile){
                this.$emit('close');
            }
        }
    },
}
</script>

<style scoped lang="scss">
    ul{
        list-style: none;
        padding-left: 0;
        margin-bottom: 0;
        li{
            display: inline-block;
            font-family: $font-paragraphs;
            &:not(:first-child){
                margin-left: 30px;
                @media screen and (max-width: $media-tablet) {
                    margin: 25px 0px 0 0;
                }
            }
            a{
                color: $text-color-dark;
                font-weight: 400;
                font-size: 20px;
                padding-bottom: 2px;
                @media screen and (max-width: $media-mobile) {
                    font-size: 12px;
                }
                &.is-active{
                    color: $brand-color;
                }
                &:hover{
                    text-decoration: none;
                    border-bottom: 3px solid $brand-color;
                }
            }
            @media screen and (max-width: $media-tablet) {
                display: block;
            }
        }
    }
    
</style>
