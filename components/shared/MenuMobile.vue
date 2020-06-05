<template>
    <transition name="slide-up" mode="out-in">
        <div class="wrapper" v-if="showDialog">
            <div class="menu" >
                <MenuList :mobile="true" @close="closeDialog" />
                <div class="divider"></div>
                <ContactInfo class="mobile" />
            </div>
            
        </div>
    </transition>
</template>

<script>
import MenuList from '~/components/shared/MenuList'
import ContactInfo from '~/components/shared/ContactInfo.vue'

export default {
  components: {
      MenuList,
      ContactInfo
  },
  props: {
      showDialog: Boolean
  },
  methods:{
      closeDialog(){
          this.$emit('close');
      }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    .wrapper{
        min-height: 400px;
        height:100vh;
        position: absolute;
        left: 0;  
        top: $menu-height-tablet;
        width: 100%;
        background-color: $main-bg-color;
        z-index: 8;
        box-shadow: 0px 3px 6px rgba(0,0,0,0.07059) inset;
        @media screen and (max-width: $media-mobile) {
            top: $menu-height-mobile;
        }
    }
    .menu{
        padding: 35px 0 35px 25px;
    }
    .md-icon-button{
        position: absolute;
        top: 10px;
        right: 30px;
    }
    .divider{
        border-bottom: 1px solid $text-color-dark;
        width: 96%;
        margin: 30px 0px 30px 0px;
    }
    .mobile.lang{
        max-width: 60px;
    }
   
    


/* slide from up to down */
.slide-up-leave-active {
    animation: slide-out-up .4s linear;
}

.slide-up-enter-active {
    animation: slide-in-up .4s linear forwards;
}

.slide-up-in-leave-active {
    animation: slide-out-up .4s linear;
}

.slide-up-leave {
    opacity: 1;
    transform: translateY(-100%);
}

@keyframes slide-out-up {
    0% {
        transform: translateY(0);
    }
    70% {
        transform: translateY(-70%);
    }
    90% {
        transform: translateY(-90%);
    }
    100% {
        transform: translateY(-100%);
    }
}
@keyframes slide-in-up {
    0% {
        transform: translateY(-100%);
    }
    70% {
        transform: translateY(0);
    }
    90% {
        transform: translateY(0);
    }
    100% {
        transform: translateY(0);
    }
}
</style>
