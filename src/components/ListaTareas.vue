<template>
    <div>
        <table>
            <thead>
                <tr>
                    <th>
                        Nombre de la Tarea
                    </th>
                </tr>
            </thead>
            <tbody>
                <Tarea v-for="tarea in tareas" :key="tarea">{{ tarea.tarea }}</Tarea>
            </tbody>
        </table>
        
    </div>
</template>

<script>
    import Tarea from './Tarea.vue';

    export default{
        components:{
            Tarea

        },
        data(){
            return{
                tareas: [
                    {tarea:'Hacer de comer', terminada: false},
                    {tarea:'Hacer tarea de Mate', terminada: false},
                    {tarea:'Hacer las compras', terminada: false},
                    {tarea:'Hacer la tarea de ciencia', terminada: false},
                ],
            }
        },
    }
</script>

<style>
table, th, tr {
  border: 1px solid black;
}
</style>
