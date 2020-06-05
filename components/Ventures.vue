<template>
    <a-layout class="outer-wrapper">
        <a-layout-content class="wrapper">
          <h2 v-scroll-reveal>Featured Business Ventures</h2>
        </a-layout-content>
    </a-layout>
</template>

<script>

export default {
    components: {
        
    },
}
</script>

<style scoped lang="scss">
    .outer-wrapper{
        background-color: #FFFFFF;
        padding: 150px 0;
        @media screen and (max-width: $media-tablet) {
            padding: 90px 0;
        }
    }
    
</style>
