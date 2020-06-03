<template>
    <div class="media text-muted pt-3" id="r-5ccb9cf62bf5940ea2299e33" style="user-select: auto;">
        <svg class="bd-placeholder-img mr-2 rounded" width="32" height="32" xmlns="http://www.w3.org/2000/svg"
             preserveAspectRatio="xMidYMid slice" focusable="false" role="img" aria-label="Placeholder: 32x32"
             style="user-select: auto;">
            <title style="user-select: auto;"></title>
            <rect width="100%" height="100%" fill="#007bff" style="user-select: auto;"></rect>
            <text x="50%" y="50%" fill="#007bff" dy=".3em" style="user-select: auto;">32x32</text>
        </svg>
        <div class="media-body pb-3 mb-0 small lh-125 border-bottom border-gray" style="user-select: auto;">
            <div class="d-flex justify-content-between align-items-center w-100" style="user-select: auto;">
                <strong class="text-gray-dark" style="user-select: auto;">한솥도시락</strong>
                <a href="#" v-on:click="onClickRemove('5ccb9cf62bf5940ea2299e33', '한솥도시락', data)" style="user-select: auto;">삭제</a>
            </div>
            <span class="d-block" style="user-select: auto;">
                <span style="user-select: auto;">{{data}}</span>번 방문 /
                <span style="user-select: auto;">124</span>번 선택
            </span>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Restaurant",
        props: {
            data: Number,
        },
        methods: {
            onClickRemove(seq, name, type) {
                console.log("seq => ", seq);
                console.log("name => ", name);
                console.log("type => ", type);
            }
        }
    }
</script>

<style scoped>

</style>