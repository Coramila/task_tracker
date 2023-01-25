<template>
    <Box>
        <div class="columns">
            <div class="column is-4">
                {{ tarefa.descricao || "Tarefa sem descrição" }}
            </div>
            <div class="column is-3">
                {{ tarefa.projeto?.nome || 'N/D' }}
            </div>
            <div class="column">
                <cronometro :tempoEmSegundos="tarefa.duracaoEmSegundos" />
            </div>
        </div>
    </Box>
</template>

<script lang="ts">
import { defineComponent, PropType } from 'vue';
import cronometro from "./cronometro.vue";
import ITarefa from "../interfaces/ITarefa"
import Box from './Box.vue'

export default defineComponent({
    name: 'TarefaTarefa',
    components: {
        cronometro,
        Box
    },
    props: {
        tarefa: {
            type: Object as PropType<ITarefa>,
            required: true

        }
    }
});
</script>

