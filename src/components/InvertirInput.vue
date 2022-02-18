<template >
    <div>
        <h2>Invertir un input</h2>
        <input type="text" v-model="message" placeholder="ingrese un texto">
        
        <p>{{ invertirCadena }}</p>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                message: '',
            }
        },
        computed: {
            invertirCadena(){
                return this.message.split('').reverse().join('');
            }
        },
    };
</script>