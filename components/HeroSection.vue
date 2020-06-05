<template>
    <a-layout>
        <a-layout-content class="wrapper">
            <div class="text-wrapper">
                <h1>Stephan Akerboom</h1>
                <span>Entrepreneur and Angel Investor</span>
                <div class="btn-group">
                    <button class="btn btn-transparent btn-outline">
                        <a href="#" v-scroll-to="'#checklist'">Investment Requirements</a>
                    </button>  
                    <button class="btn btn-outline">
                        <a href="#" v-scroll-to="'#contacts'">Apply Now</a>
                    </button>
                </div>
            </div>
           
        </a-layout-content>
    </a-layout>
</template>

<script>
export default {

}
</script>

<style scoped lang="scss">
    .wrapper{
        height: 100%;
        align-items: center;
        display: flex;
    }

    .text-wrapper{
        padding: 150px 0;
        @media screen and (max-width: $media-mobile) {
            max-width: 300px;
        }
        h1,span{
            @media screen and (max-width: $media-tablet) {
                max-width: 350px;
            }
        }
        .btn-group{
            margin-top: 80px;
            @media screen and (max-width: $media-mobile) {
                margin-top: 30px;
            }
            >:first-child{
                margin-right: 30px;
                @media screen and (max-width: $media-mobile) {
                    margin-bottom: 50px;
                }
            }
        }
        span{
            color: #707070;
            font-size: 35px;
            display: inline-block;
            line-height: 47px;
            font-family: $font-paragraphs;
            @media screen and (max-width: $media-mobile) {
                font-size: 20px;
                line-height: 27px;
            }
        }
    }
</style>
