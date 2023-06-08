<script>
import MyButton from './UI/MyButton.vue';
import MyModal from './UI/MyModal.vue';
import Status from './UI/Status.vue';

export default {
    components: { MyButton, MyModal, Status },
    data() {
        return {
            dialoVisible: false,
        }
    },
    methods: {
        showDialog() {
        this.dialoVisible = true
      },
      closeDialog() {
        this.dialoVisible = false
      },
    }
}
</script>

<template>
    <div class="header">
        <div class="header_logo">
            <img src="/logo.svg" alt="logo">
            <MyButton class="status">свободен</MyButton>
        </div>
        <MyButton v-if="!dialoVisible" @click="showDialog">СВЯЗАТЬСЯ</MyButton>
        <button v-else @click="closeDialog" class="btn__close"><svg class="svg" width="36" height="36" viewBox="0 0 36 36" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M0.499998 18C0.499999 8.33502 8.33502 0.500001 18 0.500002C27.665 0.500003 35.5 8.33502 35.5 18C35.5 27.665 27.665 35.5 18 35.5C8.33501 35.5 0.499997 27.665 0.499998 18Z" stroke="#21E6C1"/>
        <path class="line" d="M27.8994 27.8995L8.10042 8.10055" stroke="#21E6C1" stroke-width="4"/>
        <line class="line" x1="8.10044" y1="27.8995" x2="27.8994" y2="8.10055" stroke="#21E6C1" stroke-width="4"/>
</svg></button>
        <my-modal :show="dialoVisible"></my-modal>
    </div>
</template>

<style>
.header {
    display: flex;
    justify-content: space-between;
    margin-top: 11px;
}
.status {
    position: absolute !important;
    right: -71px;
    font-size: 10px !important;
    top: -3px;
    padding: 2px 4px !important; 
}
@media (max-width: 704px) {
    .status {
    right: 88px;
    top: 32px;

}
}
.header_logo {
    display: flex;
    position: relative;
}
.btn__close {
    background: transparent;
    border: none;
    cursor: pointer;
}
.btn__close:hover .svg {
    fill: #21E6C1;
    transition: 0.9s;
}
.btn__close:hover .line {
    stroke: #020303;
    transition: 0.9s;
}
</style>