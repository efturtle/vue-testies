<template>
    <div>
        <input class="border" type="text" v-model="coupon" placeholder="ingrese un cupon">
        <button class="border bg-gray-300" @click="applied">Aplicar Cupon</button>
    </div>
</template>
<script>
export default {
    data(){
        return{
            coupon: '',
        }
    },
    methods:{
        applied(){
            this.$emit('applied')
        }
    },
}
</script>