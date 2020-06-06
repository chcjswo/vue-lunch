<template>
    <div class="media text-muted pt-3">
        <svg class="bd-placeholder-img mr-2 rounded" width="32" height="32" xmlns="http://www.w3.org/2000/svg"
             preserveAspectRatio="xMidYMid slice" focusable="false" role="img" aria-label="Placeholder: 32x32"
            >
            <title></title>
            <rect width="100%" height="100%" fill="#007bff"></rect>
            <text x="50%" y="50%" fill="#007bff" dy=".3em">32x32</text>
        </svg>
        <div class="media-body pb-3 mb-0 small lh-125 border-bottom border-gray text-left">
            <div class="d-flex justify-content-between align-items-center w-100">
                <strong class="text-gray-dark">한솥도시락</strong>
                <a href="#" v-on:click="onClickRemove('5ccb9cf62bf5940ea2299e33', '한솥도시락', data)">삭제</a>
            </div>
            <span class="d-block">
                <span>{{data}}</span>번 방문 /
                <span>124</span>번 선택
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