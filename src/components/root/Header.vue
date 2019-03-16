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
</style>
