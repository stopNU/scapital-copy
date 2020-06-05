<template >
    <nav class="menu-wrapper" v-bind:class="{ mobile: showDialog }">
        <MenuMobile :showDialog="showDialog" @close="close" />
        <div class="menu content">
            <div class="logo">
                <scrollactive :offset="100">
                    <a href="#home" class="scrollactive-item">
                        <img src="~@/assets/icons/scapital_glyph.svg" class="show-mobile" alt="">
                        <LogoColor class="hide-mobile" />
                    </a> 
                </scrollactive>
            </div>
            <MenuList class="hide-tablet" />
            <div class="show-tablet mobile-menu" @click="toggle()" >
                <HamburgerMenu v-if="!showDialog" />
                <a-icon type="close" class="close" v-if="showDialog" />
            </div>
        </div>
    </nav>
</template>

<script>
import HamburgerMenu from '~/components/shared/HamburgerMenu'
import MenuMobile from '~/components/shared/MenuMobile'
import MenuList from '~/components/shared/MenuList'
import LogoColor from '~/components/shared/LogoColor.vue'

export default {
  components: {
      HamburgerMenu,
      MenuMobile,
      MenuList,
      LogoColor
  },
  data() {
    return {
            showDialog: false
        }
    },
    methods:{
        toggle(){
            this.showDialog = !this.showDialog;
        },
        close(){
            this.showDialog = false;
        }
    },
}
</script>

<style scoped lang="scss">
    .menu-wrapper{
        height: $menu-height;
        background-color: #FFFFFF;
        width: 100%;
        padding: 0 20px;
        @media screen and (max-width: $media-tablet) {
            height: $menu-height-tablet;
            padding: 0 $side-padding-tablet;
        }
        @media screen and (max-width: $media-mobile) {
            height: $menu-height-mobile;
            padding: 0 $side-padding-mobile;
        }
        &.mobile{
            background-color: $main-bg-color;
        }
    }
    .mobile-menu{
        position: absolute;
        right: 15px;
        display: flex;
        align-items: center;
        .close{
            font-size: 20px;
            color: $text-color-dark;
            font-weight: bold;
            cursor: pointer;
        }
    }
    .menu{
        margin: 0 auto;
        display: flex;
        align-items: center;
        height: 100%;
        .logo{
            a{
                vertical-align: text-top;
            }
            flex: 1;
            img{
                max-width: 210px;
            }
            @media screen and (max-width: $media-tablet) {
                height: 48px;
                display: flex;
                align-items: center;
                margin: 0 auto;
            }
        }
        
    }
</style>
