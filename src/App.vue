<template>
    <div id="app" class="col-md-6 order-md-1">
        <Header />
        <TodayLunch />
        <div class="my-3 p-3 bg-white rounded shadow-sm restaurantList">
            <h6 class="border-bottom border-gray pb-2 mb-0 text-left">등록된 식당 목록</h6>
            <Restaurant v-for="(item, i) in this.restaurantList" :key="i" :item="item" />
        </div>
        <Choice />
        <div class="col-md-6" style="height: 10px"></div>
        <Regist />
        <Footer />
    </div>
</template>

<script>
    import Header from './components/Header';
    import TodayLunch from "./components/TodayLunch";
    import Restaurant from "./components/Restaurant";
    import Choice from "./components/Choice";
    import Regist from "./components/Regist";
    import Footer from "./components/Footer";

    import axios from 'axios';

    export default {
        name: 'App',
        components: {
            Header,
            TodayLunch,
            Restaurant,
            Choice,
            Regist,
            Footer
        },
        data() {
            return {
                restaurantList: null
            }
        },
        mounted() {
            axios.get('https://lunch.mocadev.me/api/v2/lunch/')
                .then((response) => {
                    this.restaurantList = response.data.restaurantList;
                }).catch((err) => {
                    console.log('Error 발생: ', err);
                });
        }
    }
</script>

<style>
    #app {
        font-family: Avenir, Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        margin-top: 60px;
    }
</style>
