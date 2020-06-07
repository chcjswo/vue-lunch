<template>
    <div class="col-md-12 order-md-3">
        <div>
            <b-spinner class="m-5" label="Loading..." v-show="loading"></b-spinner>
        </div>
        <h4 class="mb-3 text-left">식당 등록</h4>
        <button v-b-modal.modal-prevent-closing class="btn btn-dark btn-lg btn-block">식당 등록</button>
        <b-modal
                id="modal-prevent-closing"
                ref="modal"
                title="식당 등록"
                @show="resetModal"
                @hidden="resetModal"
                @ok="handleOk"
                centered
        >
            <form ref="form" @submit.stop.prevent="handleSubmit">
                <b-form-group
                        :state="nameState"
                        label-for="name-input"
                        invalid-feedback="식당을 이름을 입력해 주세요."
                >
                    <b-form-input
                            id="name-input"
                            v-model="name"
                            :state="nameState"
                            placeholder="식당 이름"
                            required
                    ></b-form-input>
                </b-form-group>
            </form>
        </b-modal>
    </div>
</template>

<script>

    export default {
        name: "Regist",
        data() {
            return {
                name: '',
                nameState: null,
                loading: false
            }
        },
        methods: {
            addRestaurant() {
                // Exit when the form isn't valid
                if (!this.checkFormValidity()) {
                    return;
                }
                alert(this.name);
                this.loading = true;
                // Hide the modal manually
                this.closeModal();
            },
            checkFormValidity() {
                const valid = this.$refs.form.checkValidity();
                this.nameState = valid;
                return valid;
            },
            resetModal() {
                this.name = '';
                this.nameState = null;
                this.loading = false;
            },
            handleOk(bvModalEvt) {
                // Prevent modal from closing
                bvModalEvt.preventDefault();
                // Trigger submit handler
                // this.handleSubmit();
                this.addRestaurant();
            },
            handleSubmit() {
                this.closeModal();
            },
            closeModal() {
                this.$nextTick(() => {
                    this.$bvModal.hide('modal-prevent-closing')
                });
            }
        }
    }
</script>

<style scoped>

</style>