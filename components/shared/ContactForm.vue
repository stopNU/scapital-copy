<template>
    <div class="form-wrapper">
        <h3 v-scroll-reveal class="text-brand">Get in touch</h3>
        <p v-scroll-reveal>I’m inspired by the limitations technology breaks each day and eager to discuss your role in the disruptive innovation revolution. Don’t be shy, if you have a business idea you believe in, write me right away to scale it up!</p>
        <form
        action="https://formspree.io/mjvekved"
        method="POST"
        class="form-fields"
        >
            <label v-scroll-reveal>
                <input type="text" placeholder="First Name*" name="first_name">
            </label>
            <label v-scroll-reveal>
                <input type="text" placeholder="Email*" name="_replyto">
            </label>
            <label v-scroll-reveal>
                <input type="text" placeholder="Company Name*" name="company_name">
            </label>
            <label v-scroll-reveal>
                <input type="text" placeholder="Company Size*" name="company_size">
            </label>
            <label class="message" v-scroll-reveal>
                <textarea placeholder="Message" rows="5"  name="message"></textarea>
            </label>

            <button type="submit" class="btn"><a>Send</a></button>
         
        </form>
        
    </div>  
</template>

<script>

export default {
    components: {
        
    },
  methods: {
    
  }
}
</script>

<style scoped lang="scss">
    .form-wrapper{
        background-color: #FFFFFF;
        padding: 60px;
        border-top-left-radius: $border-radius-style;
        border-bottom-right-radius: $border-radius-style;
        box-shadow: 0px 3px 86px #00000029;
        h3{
            @media screen and (max-width: $media-mobile) {
                font-size: 25px;
                line-height: 30px;
            }
        }
    }
    .form-fields {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        column-gap: 60px;
        row-gap: 30px;
        margin-top: 30px;
        label{
            input, textarea{
                width: 100%;
                border: none;
                border-bottom: 1px solid $brand-color;
                font-size: 17px;
                font-family: $font-paragraphs;
                padding: 3px;
                @media screen and (max-width: $media-mobile) {
                    font-size: 12px;
                }
            }
            textarea{
                border: 1px solid $brand-color;
            }
        }
        .message{
            grid-column: span 2;
            margin-top: 45px;
            margin-bottom: 60px;
            @media screen and (max-width: $media-mobile) {
                margin-top: 15px;
                margin-bottom: 30px;
            }
        }
        .btn{
            outline: none;
            text-align: left;
        }
    }
</style>
