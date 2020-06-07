<template>
    <div class="col-md-12 order-md-2">
        <h4 class="mb-3 text-left">식당 선택</h4>
        <div class="mb-3"></div>
        <button class="btn btn-info btn-lg btn-block choiceRestaurant" v-on:click="choiceModal = !choiceModal">랜덤 식당 선택</button>
        <b-modal id="modal-scoped" v-model="choiceModal">
            <template>
                <!-- Emulate built in modal header close button action -->
                <h5>점심 선택??</h5>
            </template>

            <template>
                <p>오늘은 돈까스 어떤가요???</p>
            </template>

            <template v-slot:modal-footer="{ ok, cancel, hide }">
                <!-- Emulate built in modal footer ok and cancel button actions -->
                <b-button size="sm" variant="secondary" @click="ok()" v-on:click="reChoice">
                    다시 선택
                </b-button>
                <b-button size="sm" variant="success" @click="cancel()" v-on:click="lunchChoice">
                    결정
                </b-button>
                <!-- Button with custom close trigger value -->
                <b-button size="sm" variant="danger" @click="hide()">
                    닫기
                </b-button>
            </template>
        </b-modal>
    </div>
</template>

<script>
    export default {
        name: "Choice",
        methods: {
            lunchChoice() {
                alert('lunchChoice');
            },
            reChoice() {
                alert('reChoice');
            }
        },
        data() {
            return {
                choiceModal: false
            }
        }
    }
</script>

<style scoped>

</style>