<template>
  <a-layout class="site-wrapper">
    <a-layout-header class="header">
      <Menu />
    </a-layout-header>
    <a-layout-content class="content">
      <HeroSection class="fullscreen-bg" id="home" />
      <About id="about-me" />
      <div class="bg-wrapper">
      <Philosophy />
      <Startups id="entrepreneurs" />
      </div>
      <Checklist id="checklist" />
      <Ventures id="projects" />
      <Contact id="contacts" />
    </a-layout-content>
    <a-layout-footer class="footer-wrapper">
      <a-layout class="footer wrapper">
        <img src="~@/assets/icons/scapital_logo_white.svg" class="logo" alt="SCApital white logo">
        <span class="text-light" v-scroll-reveal>© SCApital {{ new Date().getFullYear() }}. All Rights Reserved.</span>
      </a-layout>
    </a-layout-footer>
  </a-layout>
</template>

<script>
import Menu from '~/components/shared/Menu.vue'
import HeroSection from '~/components/HeroSection.vue'
import About from '~/components/About.vue'
import Philosophy from '~/components/Philosophy.vue'
import Startups from '~/components/Startups.vue'
import Checklist from '~/components/Checklist.vue'
import Ventures from '~/components/Ventures.vue'
import Contact from '~/components/Contact.vue'

export default {
  components: {
    Menu,
    HeroSection,
    About,
    Philosophy,
    Startups,
    Checklist,
    Ventures,
    Contact
  },
  head () {
    return {
      title: 'SCApital - Stephan Akerboom',
      meta: [
        // hid is used as unique identifier. Do not use `vmid` for it as it will not work
        { hid: 'description', name: 'description', content: 'Entrepreneur and Angel Investor.' }
      ]
    }
  },
  mounted(){
      //Fullscreen
      let vh = window.innerHeight * 0.01;
      // Then we set the value in the --vh custom property to the root of the document
      document.documentElement.style.setProperty('--vh', `${vh}px`);

      window.addEventListener('resize', () => {
      // We execute the same script as before
      let vh = window.innerHeight * 0.01;
      document.documentElement.style.setProperty('--vh', `${vh}px`);
    });
  }
}
</script>

<style scoped lang="scss">
  .header, .ant-layout-header{
    position: fixed;
    height: $menu-height;
    width: 100%;
    z-index: 100;
    background-color: #FFFFFF;
    padding: 0;
    box-shadow: 0px 3px 6px #00000012;
    @media screen and (max-width: $media-tablet) {
      height: $menu-height-tablet;
      //padding: 0 $side-padding-tablet;
    }
    @media screen and (max-width: $media-mobile) {
      height: $menu-height-mobile;
    }
  }
  .footer-wrapper{
    background-color: $brand-color;
    padding: 0;
    .footer{
      background: transparent;
      padding: 80px 0 50px;
      display: grid;
      grid-template-columns: repeat( 2, minmax(250px, 1fr) );
      align-items: baseline;
      @media screen and (max-width: $inner-wrapper-size) {
        padding: 80px 25px 50px;
      }
      @media screen and (max-width: $media-tablet) {
        padding: 100px 25px 30px;
      }
      @media screen and (max-width: $media-mobile) {
        padding: 30px $side-padding-mobile;
        grid-template-columns: 1fr;
        .logo{
          max-width: 160px;
        }
      }
      span{
        text-align: right;
        font-size: 20px;
        font-family: $font-paragraphs;
        line-height: 26px;
        @media screen and (max-width: $media-mobile) {
          text-align: left;
          font-size: 12px;
          line-height: 18px;
          margin-top: 30px;
        }
      }
    }
  }

  .bg-wrapper{
    background-repeat: no-repeat;
    background-image: url('~@/assets/images/MBP_section_desk.png');   
    background-image: image-set(url('~@/assets/images/MBP_section_desk.png') 1x,
                                url('~@/assets/images/MBP_section_desk@2x.png') 2x ); 
    //min-height: 940px;
    //background-size: 100%;
    @media screen and (max-width: $media-tablet) {  
    //min-height: 1000px;
      background-size: 100% 1200px;
      background-position: top center;
      background-image: url('~@/assets/images/MBP_section_tab.png');   
      background-image: image-set(url('~@/assets/images/MBP_section_tab.png') 1x,
                                    url('~@/assets/images/MBP_section_tab@2x.png') 2x ); 
    }
    @media screen and (max-width: $media-mobile) {
      background-size: 100% 1100px;
      background-image: url('~@/assets/images/MBP_section_mob.png');   
      background-image: image-set(url('~@/assets/images/MBP_section_mob.png') 1x,
                                url('~@/assets/images/MBP_section_mob@2x.png') 2x ); 
    }
  }

  .bg-wrapper, #contacts{
    @media screen and (max-width: $media-mobile) {
      
    }
  }

  .site-wrapper{
    overflow: hidden;
  }
 
  .fullscreen-bg{
    position: relative;
    background-color: #FFF;
    background-image: url('~@/assets/images/home_section_bg_desk.png');   
    background-image: image-set(url('~@/assets/images/home_section_bg_desk.png') 1x,
                                url('~@/assets/images/home_section_bg_desk@2x.png') 2x ); 
    @media screen and (max-width: $media-tablet) {  
      background-image: url('~@/assets/images/home_section_bg_tab.jpg');   
      background-image: image-set(url('~@/assets/images/home_section_bg_tab.jpg') 1x,
                                    url('~@/assets/images/home_section_bg_tab@2x.jpg') 2x ); 
    }
    @media screen and (max-width: $media-mobile) {
      background-image: url('~@/assets/images/home_section_bg_mob.jpg');   
      background-image: image-set(url('~@/assets/images/home_section_bg_mob.jpg') 1x,
                                  url('~@/assets/images/home_section_bg_mob@2x.jpg') 2x ); 
    } 
  }
</style>
