<template>
    <div>
        <button @click="showModal = true">Dale click</button>
        <Modal v-if="showModal" @close="showModal = false"></Modal>
    </div>
</template>
<script>
import Modal from './Modal.vue';
export default {
    components:{
        Modal
    },
    data(){
        return {
            showModal: false,
        }
    },
}
</script>