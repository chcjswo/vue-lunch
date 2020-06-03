<template>
    <div class="col-md-6 order-md-3" style="user-select: auto;">
        <h4 class="mb-3" style="user-select: auto;">식당 등록</h4>
        <div class="mb-3" style="user-select: auto;">
            <div class="input-group" style="user-select: auto;">
                <div class="input-group-prepend" style="user-select: auto;"></div>
                <span class="input-group-text" style="user-select: auto;">@</span>
                <input class="form-control"
                       id="restaurantName" type="text"
                       placeholder="식당 이름"
                       style="user-select: auto;">
            </div>
        </div>
        <button class="btn btn-dark btn-lg btn-block addRestaurant" style="user-select: auto;">등록</button>
    </div>
</template>

<script>
    export default {
        name: "Regist"
    }
</script>

<style scoped>

</style>