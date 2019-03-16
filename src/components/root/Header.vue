<template>
    <div class="header">
        <!-- Navigation -->
        <nav class="navbar navbar-expand-lg navbar-light fixed-top" id="mainNav">
            <div class="container">
            <button class="navbar-toggler navbar-toggler-right" type="button" data-toggle="collapse" data-target="#navbarResponsive" aria-controls="navbarResponsive" aria-expanded="false" aria-label="Toggle navigation">
                Menu
                <i class="fas fa-bars"></i>
            </button>
            <div class="collapse navbar-collapse" id="navbarResponsive">
                <ul class="navbar-nav ml-auto">
                <li class="nav-item">
                    <router-link to="/">Home</router-link>
                </li>
                <li class="nav-item">
                    <router-link to="/about">About</router-link>
                </li>
                </ul>
            </div>
            </div>
        </nav>

        <!-- Page Header -->
        <header class="masthead" style="background-image: url('img/home-bg.jpg')">
            <div class="overlay"></div>
            <div class="container">
            <div class="row">
                <div class="col-lg-8 col-md-10 mx-auto">
                    <div class="site-heading text-center">
                        <h1>Mic Koan</h1>
                    </div>
                    <div class="bg mx-auto text-center">
                        <img alt="Mickoan mic" src="../../assets/mickoan.png">
                    </div>
                </div>
            </div>
            </div>
        </header>
    </div>
 </template>

<style lang="sass">
    @import "../../assets/scss/abstracts/functions"
    @import "../../assets/scss/main"
    @import "../../assets/scss/layout/header"

    .bg
        position: absolute
        top: 300%
        left: 50%
        transform: translate(-50%, 100%)
        width: 100%
        height: 100%

    .nav-item
        margin-left: 1rem

    .site-heading
        h1
            color: $white

    .navigation
    
        label
            user-select: none
            
        p, li
            line-height: 2rem

        .active:before
            content: ""
            position: absolute
            width: 100%
            height: 2px
            bottom: 0
            left: 0
            background-color: $color-white
            visibility: visible
            -webkit-transform: scaleX(1)
            transform: scaleX(1)

        &__checkbox
            display: none
        

        &__button
            background-color: $color-white
            height: 7rem
            width: 7rem
            position: absolute
            top: 3rem
            right: 2rem
            border-radius: 50%
            z-index: 2000
            box-shadow: 0 1rem 3rem rgba($color-black, .1)
            text-align: center
            cursor: pointer

            @include respond(tab-port)
                top: 2.8rem
                right: 2rem
            

            @include respond(phone)
                top: 3rem
                right: 3rem
            
        

        &__background
            height: 95vh
            min-width: 320px
            border-radius: 5rem
            width: 100%
            position: absolute
            top: 3rem 
            right: 2.5rem
            background-image: radial-gradient($color-primary-light, $color-primary-dark)
            z-index: 1000
            transition: transform .8s cubic-bezier(0.86, 0, 0.07, 1)

            @include respond(tab-port)
                top: 3.3rem
                right: 2.5rem
            

            @include respond(phone)
                top: 3.5rem
                right: 3.5rem
            
        

        &__nav
            height: 100vh
            position: absolute
            top: 0
            right: 0
            z-index: 1500
            opacity: 0
            width: 0
            transition: all .8s cubic-bezier(0.68, -0.55, 0.265, 1.55)
        

        &__list
            position: absolute
            +center-xy()
            list-style: none

            @include respond(tab-land-height)
                height: 100%
                overflow-y: scroll

            h1
                font-size: 4rem
                margin-top: 5rem
                color: $color-white
        

        &__item
            margin: 1rem

        &__link
            &:link,
            &:visited
                display: inline-block
                font-size: 18px
                font-weight: 300
                padding: 1rem 2rem
                color: $color-white
                text-decoration: none
                position: relative

                span
                    margin-right: 1.5rem
                    display: inline-block
                
            &:before
                content: ""
                position: absolute
                width: 100%
                height: 2px
                bottom: 0
                left: 0
                background-color: $color-white
                visibility: hidden
                -webkit-transform: scaleX(0)
                transform: scaleX(0)
                -webkit-transition: all 0.3s ease-in-out 0s
                transition: all 0.3s ease-in-out 0s

            &:hover:before
                visibility: visible
                -webkit-transform: scaleX(1)
                transform: scaleX(1)

        //FUNCTIONALITY
        &__checkbox ~ &__background
            transform: scale(0)

        &__checkbox:checked ~ &__background
            transform: scale(1)
        

        &__checkbox:checked ~ &__nav
            opacity: 1
            width: 100%

        // &__checkbox:checked ~ &__button, &__background
        //     transform: translate(26rem, -26rem)

        


        //ICON
        &__icon
            position: relative
            margin-top: 3.5rem

            &,
            &::before,
            &::after
                width: 3rem
                height: 2px
                background-color: $color-grey-dark-3
                display: inline-block
            

            &::before,
            &::after
                content: ""
                position: absolute
                left: 0
                transition: all .2s
            

            &::before
                top: -.8rem 
            &::after
                top: .8rem 
        

        &__button:hover &__icon::before
            top: -1rem
        

        &__button:hover &__icon::after
            top: 1rem
        

        &__checkbox:checked + &__button &__icon
            background-color: transparent
        

        &__checkbox:checked + &__button &__icon::before
            top: 0
            transform: rotate(135deg)
        

        &__checkbox:checked + &__button &__icon::after
            top: 0
            transform: rotate(-135deg)
</style>
