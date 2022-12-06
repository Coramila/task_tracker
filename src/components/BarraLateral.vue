<template>
<header>
    <h1>
        <img src="../assets/logo_.png" alt="">
    </h1>
</header>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent ({
    name: 'BarraLateral'
})
</script>

<style scoped>

header{
    background-color: rgb(0 74 173);
    width: 100%;
    height: 100vh;
}

header img {
    border-radius: 30px;
    /* margin: 1rem; */
    scale: calc(0.9);
}

@media only screen and (max-width: 768px){
    header {
        padding: 2.5rem;
        height: auto;
    }
}

</style>