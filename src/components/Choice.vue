<template>
    <div class="col-md-12 order-md-2">
        <h4 class="mb-3 text-left">식당 선택</h4>
        <div class="mb-3"></div>
        <button class="btn btn-info btn-lg btn-block choiceRestaurant" v-on:click="lunchChoice">랜덤 식당 선택</button>
    </div>
</template>

<script>
    export default {
        name: "Choice",
        methods: {
            lunchChoice() {
                console.log('lunchChoice');
            }
        }
    }
</script>

<style scoped>

</style>