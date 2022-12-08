<template>
    <div class="box has-text-wueight-bold">
        <div class="columns">
            <div class="column is-7">
                {{tarefa.descricao}}
            </div>
            <div class="column">
                <cronometro :tempoEmSegundos="tarefa.duracaoEmSegundos" />
            </div>
        </div>
    </div>
</template>

<script lang="ts">
import { defineComponent, PropType } from 'vue';
import cronometro from "./cronometro.vue";
import ITarefa from "../interfaces/ITarefa"

export default defineComponent ({
    name: 'TarefaTarefa',
    components:{
        cronometro,
    },
    props:{
        tarefa: {
            type: Object as PropType < ITarefa >,
             required: true   
                
        }
    }
});
</script>

<style scoped>
.box{
    background-color: #ebe6e6 ;
}
</style>