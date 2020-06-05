<template>
    <a-layout class="outer-wrapper">
        <div class="top-curv-bar"></div>
        
        <a-layout-content class="wrapper">
            <span class="background-text">Contacts</span>
            <h2 v-scroll-reveal>Contacts</h2>
            <div class="separator"></div>
            <div class="grid">
                <ContactInfo />
                <div class="form">
                    <ContactForm />
                </div>  
            </div>        
        </a-layout-content>
    </a-layout>
</template>

<script>
import ContactForm from '~/components/shared/ContactForm.vue'
import ContactInfo from '~/components/shared/ContactInfo.vue'

export default {
    components: {
        ContactForm,
        ContactInfo
    },
}
</script>

<style scoped lang="scss">
    $spillover: 15px;
    $spillover-tablet: $spillover*3;

    .form{
        @media screen and (max-width: $media-mobile) {
            background: rgb(243,243,243);
            background: linear-gradient(180deg, rgba(243,243,243,1) 37%, rgba(10,113,255,1) 65%, rgba(10,113,255,1) 100%);
        }   
    }

    .grid{
        display: grid;
        grid-template-columns: 1fr 1fr;
        @media screen and (max-width: $media-tablet) {
            grid-template-columns: 1fr;
        }
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
    }
    .outer-wrapper{
        background-color: #F3F3F3;
        position: relative;
        padding: 210px-$spillover 0 0px;
        box-shadow: 0 -5px 9px -3px #00000029;
        @media screen and (max-width: $media-tablet) {
            padding: 150px-$spillover-tablet 0 0px;
        }
        @media screen and (max-width: $media-mobile) {
            padding: 90px-$spillover-tablet 0 0px;
        }
        .wrapper{
            position: relative;
            top: $spillover;
            @media screen and (max-width: $media-tablet) {
                row-gap: 60px;
                top: $spillover-tablet;
            }
            @media screen and (max-width: $media-mobile) {
                padding: 30px 0 0;
                top: 0;
            }
            .background-text{
                position: absolute;
                top: -100px;
                @media screen and (max-width: $media-mobile) {
                    top: -30px;
                }
            }
        }
    }
    .separator{
        margin-bottom: 30px;
        @media screen and (max-width: $media-mobile) {
            margin: 0 $side-padding-mobile 30px;
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
    h2,.background-text, .grid .info{
        @media screen and (max-width: $media-mobile) {
            padding: 0 $side-padding-mobile;
        }
    }
</style>
