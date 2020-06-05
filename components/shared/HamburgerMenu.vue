<template>
    <div class="hamburger hamburger--slider js-hamburger">
        <div class="bg-black hamburger-box"> 
            <div class="hamburger-inner"></div>
        </div>
    </div>
</template>

<script>

export default {
  name: 'HamburgerMenu',
}
</script>

<style lang="scss">
.hamburger-box {
    padding: 12px 20px 12px 20px;
    cursor: pointer;
}
.hamburger-box {
    position: relative;
    display: inline-block;
    width: 50px;
    height: 50px;
}



.hamburger-inner, .hamburger-inner:after, .hamburger-inner:before {
    position: absolute;
    width: 20px;
    height: 2px;
    transition-timing-function: ease;
    transition-duration: .15s;
    transition-property: transform;
    background-color: $text-color-dark;
}
.hamburger-inner {
    top: 50%;
    display: block;
    margin-top: -2px;
}
.hamburger--slider .hamburger-inner {
    top: 23px;
}   


.hamburger-inner:after, .hamburger-inner:before {
    display: block;
    content: "";
}

.hamburger-inner:before {
    top: -10px;
}

.hamburger--slider .hamburger-inner:before {
    top: 6px;
    transition-timing-function: ease;
    transition-duration: .15s;
    transition-property: transform,opacity;
}

.hamburger--slider .hamburger-inner:after {
    top: 12px;
}

</style>
