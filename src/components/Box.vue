<template>
    <div class="box has-text-wieght-bold">
        <slot></slot>
    </div>
</template>

<script lang="ts">
    import { defineComponent } from 'vue';

    export default defineComponent ({
        name: 'BoxTarefa'
    })
</script>

<style scoped>
.box{
    background-color: #ebe6e6 ;
    margin: 1rem;
}
</style>