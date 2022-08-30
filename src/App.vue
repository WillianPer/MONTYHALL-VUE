<template>
    <div id="app">
        <h1>Problema de Monty Hall</h1>
        <DoorVue number="1" :has-gift="false"/>
    </div>
</template>

<script>


import DoorVue from './components/DoorVue.vue';

export default {
    name: "app",
    components: { DoorVue }
}
</script>

<style>
    * {
        box-sizing: border-box;
        font-family: 'Montserrat', sans-serif;
    }
    body {
        color: #fff;
        background: linear-gradient(to right, rgb(21, 153, 87), rgb(21, 87, 153));
    }
    #app {
        display: flex;
        flex-direction: column;
        align-items: center;
    }
    #app h1 {
        border: 1px solid #000;
        background-color: #0004;
        padding: 20px;
        margin-bottom: 60px;
    }
</style>