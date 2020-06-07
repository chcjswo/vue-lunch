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
                this.$bvModal.msgBoxConfirm(`오늘은 이미 무극라멘으로 결정 됐습니다.다시 선택 하시겠습니까?`, {
                    title: '다른게 먹고 싶어요!',
                    size: 'md',
                    buttonSize: 'sm',
                    okVariant: 'danger',
                    okTitle: '재선택',
                    cancelTitle: '그냥 먹기',
                    footerClass: 'p-2',
                    hideHeaderClose: false,
                    centered: true,
                    contentClass: 'shadow'
                })
                .then(value => {
                    alert(value);
                })
                .catch(err => {
                    // An error occurred
                    console.log(err);
                });
            }
        }
    }
</script>

<style scoped>

</style>