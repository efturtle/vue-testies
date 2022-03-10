<template>
  <div class="text-center ml-4">
    <Chiste v-for="(chiste, index) in chistes" :key="index">
        <p class="font-bold">Chiste #{{ incremento(index) }}</p>
        <p class="ml-4">{{ chiste.setup }}</p>
        <p class="ml-10"> *{{ chiste.delivery }}</p>
    </Chiste>
  </div>
</template>

<script>
import axios from "axios";
import Chiste from './Chiste.vue';
export default {
    components:{
        Chiste
    },
    data(){
        return{
            chistes: [],
            
        }
    },
    mounted(){
        axios.get('https://v2.jokeapi.dev/joke/Programming?type=twopart&amount=4')
        .then((data)=>{
            this.chistes = data.data.jokes;
        });
    },
    methods:{
        incremento(index){
            return index+1;
        }
    }
}
</script>