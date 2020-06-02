<template>
    <div class="card mb-4 shadow-sm" id="todayLunch" style="user-select: auto;">
        <div class="card-header" style="user-select: auto;"><h6 class="my-0 font-weight-normal"
                                                                style="user-select: auto;"><span id="today"
                                                                                                 style="user-select: auto;">2020-06-02 선택된 식당</span>
        </h6></div>
        <div class="card-body" style="user-select: auto;"><h5 class="card-title" id="todayRestaurant"
                                                              style="user-select: auto;">오늘은 <b
                style="user-select: auto;">양파볶음밥</b> 입니다.</h5></div>
        <div class="card-footer" style="user-select: auto;">
            <div class="btn btn-dark btn-sm reChoiceRestaurant" style="user-select: auto;">식당 재선택</div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "TodayLunch"
    }
</script>

<style scoped>

</style>