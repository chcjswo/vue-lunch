<template>
    <div id="app" class="col-md-6 order-md-1">
        <img alt="Vue logo" src="./assets/logo.png">
        <Header />
        <TodayLunch />
        <Restaurant v-for="(data, i) in 20" :key="i" :data="data" />
        <Choice />
        <Regist />
    </div>
</template>

<script>
    import Header from './components/Header';
    import TodayLunch from "./components/TodayLunch";
    import Restaurant from "./components/Restaurant";
    import Choice from "./components/Choice";
    import Regist from "./components/Regist";

    export default {
        name: 'App',
        components: {
            Header,
            TodayLunch,
            Restaurant,
            Choice,
            Regist
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
