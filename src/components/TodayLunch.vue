<template>
    <div class="card mb-4 shadow-sm" id="todayLunch">
        <div class="card-header">
            <h6 class="my-0 font-weight-normal">
                <span id="today">2020-06-02 선택된 식당</span>
            </h6>
        </div>
        <div class="card-body">
            <h5 class="card-title" id="todayRestaurant">오늘은 <b>양파볶음밥</b> 입니다.</h5>
        </div>
        <div class="card-footer">
            <div class="btn btn-dark btn-sm" v-on:click="reChoiceRestaurant">식당 재선택</div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "TodayLunch",
        methods: {
            reChoiceRestaurant() {
                console.log('reChoiceRestaurant');
            }
        }
    }
</script>

<style scoped>

</style>