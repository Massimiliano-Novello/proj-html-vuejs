<script>
import SearchBar from './SearchBar.vue';
export default {
    name: "AppHeader",
    components: {
        SearchBar
    },
    data () {
        return {
            contentNavBar: ["Home", "Mission", "Causes", "Journal", "Donate"]
        }
    }
}
</script>

<template>
    <header>
        <div class="nav-bar container d-flex justify-content-between align-items-center">
            <div class="logo">
                <img src="../assets/img/avada-charity-mobile-logo-retina.png" alt="">
            </div>
            <div class="navigation d-flex">
                <SearchBar v-for="(nav, index) in contentNavBar" :key="index" :navigationBar="nav"/>
            </div>
        </div>
        <div class="jumbotron text-white py-4">
            <h1>MAKE A DIFFERENCE</h1>
            <p class="py-3">As a long as a poverty, injustice & inequality persist, none of uscan truly rest</p>
            <div>
                <button type="button" class="btn btn-outline-info mx-2">OUR MISSIONS</button>
                <button type="button" class="btn btn-outline-warning">DONATE NOW</button>
            </div>
        </div>
    </header>

</template>

<style lang="scss" scoped>
header {
    min-height: 600px;
    background-image: url(../assets/img/home-page-slider.jpg);
    background-size: cover;
    position: relative;

    .nav-bar {
        height: 80px;

        img {
            width: 200px;
        }
    }

    .jumbotron {
        text-align: center;
        padding: 100px 0;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
    }
}
</style>