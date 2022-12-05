<template>
    <div class="box">
        <div class="columns">
            <div class="column in-8" role="form" aria-label="Formulário nova tarefa">
                <input type="text" class="input" placeholder="Qual tarefa você deseja iniciar?">
            </div>
            <div class="column">
                <section>
                    <strong>00:00:00</strong>
                </section>
                <button class="button">
            <span class="icon">
                <i class="fas fa-play"></i>
            </span>
            <span>play</span>
        </button>
        <button class="button">
            <span class="icon">
                <i class="fas fa-stop"></i>
            </span>
            <span>stop</span>
        </button>
            </div>
        </div>            
    </div>    
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent ({
    name: 'Formulario'
})
</script>
