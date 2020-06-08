<template>
    <div class="media text-muted pt-3">
        <svg class="bd-placeholder-img mr-2 rounded align-bottom" width="32" height="32" xmlns="http://www.w3.org/2000/svg"
             preserveAspectRatio="xMidYMid slice" focusable="false" role="img" aria-label="Placeholder: 32x32"
            >
            <title></title>
            <rect width="100%" height="100%" fill="#007bff"></rect>
            <text x="50%" y="50%" fill="#007bff" dy=".3em">32x32</text>
        </svg>
        <div class="media-body pb-3 mb-0 small lh-125 border-bottom border-gray text-left align-top">
            <div class="d-flex justify-content-between align-items-center w-100">
                <strong class="text-gray-dark">{{ item.name }}</strong>
                <b-button variant="outline-secondary"
                          size="sm"
                          v-on:click="onClickRemove(item._id, item.name, item.visitCount)">
                    삭제
                </b-button>
            </div>
            <span class="d-block">
                <span>{{ item.visitCount }}</span>번 방문 /
                <span>{{ item.choiceCount }}</span>번 선택
            </span>
            <b-alert v-model="showDismissibleAlert" variant="danger" dismissible class="m-1 align-middle">
                방문한적이 있는 식당은 삭제가 안됩니다.
            </b-alert>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Restaurant",
        props: {
            item: Object,
        },
        data() {
            return {
                showDismissibleAlert: false
            }
        },
        methods: {
            onClickRemove(seq, name, visitCount) {
                console.log("seq => ", seq);
                console.log("name => ", name);
                console.log("visitCount => ", visitCount);

                if (visitCount > 0) {
                    this.showDismissibleAlert = true;
                    return;
                    // notify("방문한적이 있는 식당은 삭제가 안됩니다.", "danger", 10);
                    // return;
                }

                this.$bvModal.msgBoxConfirm(`${name}을(를) 삭제 하시겠습니까?`, {
                    title: '식당 삭제',
                    size: 'sm',
                    buttonSize: 'sm',
                    okVariant: 'danger',
                    okTitle: '삭제 해!',
                    cancelTitle: '삭제 NO!',
                    footerClass: 'p-2',
                    hideHeaderClose: false,
                    centered: true
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