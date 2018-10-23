<template>
    <div class="main">
        <h1>Calculadora sencilla</h1>

        <div class="calc">
            <input type="text">
            <button id="c">C</button>
            <button id="division">/</button>
            <button id="mult">*</button>
            <button id="menos">-</button>
            <button id="siete">7</button>
            <button id="ocho">8</button>
            <button id="nueve">9</button>
            <button id="mas">+</button>
            <button id="cuatro">4</button>
            <button id="cinco">5</button>
            <button id="seis">6</button>
            <button id="uno">1</button>
            <button id="dos">2</button>
            <button id="tres">3</button>
            <button id="igual">=</button>
            <button id="cero">0</button>
            <button id="punto">.</button>
        </div>
    </div>
</template>


<script>
    export default {

    }
</script>


<style scoped>
.main {
    display: flex;
    flex-direction: column;
    align-items: center;
}
.calc {
    width: 300px;
    height: 402px;
    display: grid;
    grid-template-columns: repeat(4, 75px);
    grid-template-rows: repeat(6, 67px);
}

.calc button, input {
    margin: 2px;
}

.calc button {
    border: 2px solid #141414;
    background-color: #141414;
    transition-duration: 0.4s;
    border-radius: 2px;
    font-size: 1.2em;
    color: white;
}

.calc button:hover {
    background-color: white;
    color: #141414;
}
.calc input {
    grid-column: 1 / span 4;
}

#mas {
    grid-column-start: 4;
    grid-row: 3 / span 2;
}

#igual {
    grid-column-start: 4;
    grid-row: 5 / span 2;
}

#cero {
    grid-column: 1 / span 2;
}

</style>