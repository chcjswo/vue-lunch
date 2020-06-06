<template>
    <div class="col-md-12 order-md-3">
        <h4 class="mb-3 text-left">식당 등록</h4>
        <div class="mb-3">
            <div class="input-group">
                <div class="input-group-prepend"></div>
                <span class="input-group-text">@</span>
                <label for="restaurantName"></label>
                <input class="form-control"
                       id="restaurantName" type="text"
                       placeholder="식당 이름"
                >
            </div>
        </div>
        <button class="btn btn-dark btn-lg btn-block" v-on:click="addRestaurant">등록</button>
    </div>
</template>

<script>
    export default {
        name: "Regist",
        methods: {
            addRestaurant() {
                console.log('addRestaurant');
            }
        }
    }
</script>

<style scoped>

</style>