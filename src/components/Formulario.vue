<template>
  <div class="box">
    <div class="columns">
      <div class="column in-8" role="form" aria-label="Formulário nova tarefa">
        <input
          type="text"
          class="input"
          placeholder="Qual tarefa você deseja iniciar?"
          v-model="descricao"
        />
      </div>
      <div class="column">  
        <Temporizador @ao-temporizador-finalizado="finalizarTarefa"/>      
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import Temporizador from './Temporizador.vue'
export default defineComponent({
    name: "FormularioTarefa",
    emits: ['aoSalvarTarefa'],
    components:{
      Temporizador
    },
    data(){
      return {
        descricao: ''
      }
    },
    methods:{
      finalizarTarefa (tempoDecorrido: number) : void {
        this.$emit('aoSalvarTarefa',{
          duracaoEmSegundos: tempoDecorrido,
          descricao: this.descricao
        })
        this.descricao = ''
      }
    }    
});
</script>
