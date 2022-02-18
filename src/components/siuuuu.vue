<template>
    <div>
        <h2>Tareas a realizar</h2>
        <input type="text" placeholder="Ingrese la tarea" v-model="tarea">
        <button @click="agregarTarea">Agregar</button>

        <h3>Tareas Terminadas</h3>
        <div v-for="(tarea, index) in tareasTerminadas" :key="index">
            <ul>
                <li>{{ tarea.tarea }}</li>
                <button @click="tareaPendiente(index)">&#10227;</button> 
            </ul>
        </div>

        <h3>Tareas No Terminadas</h3>
        <div v-for="(tarea, index) in tareasNoTerminadas" :key="index">
            <ul>
                <li>{{ tarea.tarea }}</li>
                <button @click="tareaPendiente(index)">&#10227;</button> 
            </ul>
        </div>
    </div>
</template>
<script>
export default {
    data() {
        return {
            longitudDeTareas: 0,
            tareas: [],
            tarea: '',
        }
    },
    methods: {
        agregar(){
            // esta presionado y cambia a no presionado
            if (this.estaPrecionadoElBoton) {
                this.estaPrecionadoElBoton = false;
            }
            // se presiona
            this.estaPrecionadoElBoton = true;
            this.mostrarInput = this.tarea;
            
            console.log(this.tarea);
            this.tareas.push();
        },
        agregarTarea(){
            let id = this.longitudDeTareas++;
            this.tareas.push({id: id, tarea: this.tarea, terminada: false});
        }
    },
    computed: {
        tareasTerminadas(){
            return this.tareas.filter(tarea => tarea.terminada);
        },
        tareasNoTerminadas(){
            return this.tareas.filter(tarea => !tarea.terminada);
        }
    }
}
</script>
<style>
    
</style>