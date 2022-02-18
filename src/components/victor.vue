<template>
    <div>
        <input type="number" v-model="num1">
        <select v-model="operaciones">
            <option value="0">+</option>
            <option value="1">-</option>
            <option value="2">*</option>
            <option value="3">/</option>
        </select>
        <input type="number" v-model="num2">
        <button @click="calcular">=</button>
        <strong>{{ resultado }}</strong>
    </div>
</template>
<script>
export default {
    data() {
        return {
            operaciones: '0',
            resultado: '0',
            num1:0,
            num2:0,
        }
    },
    methods: {
        calcular: function(){
            switch (this.operaciones) {
                case '0' :
                    this.resultado = parseInt(this.num1) + parseInt(this.num2);
                    break;
                case '1' :
                    this.resultado = parseInt(this.num1) - parseInt(this.num2);
                    break;
                case '2' :
                    this.resultado = parseInt(this.num1) * parseInt(this.num2);
                    break;
                case '3' :
                    this.resultado = parseInt(this.num1) / parseInt(this.num2);
                    break;

            }
        }
    },
}
</script>
<style lang="">
    
</style>