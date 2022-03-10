<template>
    <div>
        <Coupon @applied="applied"> </Coupon>
        <p v-if="seAplicoCupon" class="text-gray-500">Se aplico un cupon!</p>
    </div>
</template>
<script>
import Coupon from './Coupon.vue';
export default {
    components: {
        Coupon
    },
    data(){
        return{
            seAplicoCupon: false,
        }
    },
    methods:{
        applied(){
            this.seAplicoCupon = true;
        }
    }
}
</script>