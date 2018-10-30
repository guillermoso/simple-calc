<template>
    <div class="main">
        <h1>Calculadora sencilla</h1>

        <div class="calc">
            <input type="text" v-model="num">
            <button id="c" @click="reset()">C</button>
            <button id="division" @click="dividir()">/</button>
            <button id="mult" @click="multiplicar()">*</button>
            <button id="menos" @click="restar()">-</button>
            <button id="siete" @click="capturar(7)">7</button>
            <button id="ocho" @click="capturar(8)">8</button>
            <button id="nueve" @click="capturar(9)">9</button>
            <button id="mas" @click="sumar()">+</button>
            <button id="cuatro" @click="capturar(4)">4</button>
            <button id="cinco" @click="capturar(5)">5</button>
            <button id="seis" @click="capturar(6)">6</button>
            <button id="uno" @click="capturar(1)">1</button>
            <button id="dos" @click="capturar(2)">2</button>
            <button id="tres" @click="capturar(3)">3</button>
            <button id="igual" @click="igual()">=</button>
            <button id="cero" @click="capturar(0)">0</button>
            <button id="punto">.</button>
        </div>
    </div>
</template>


<script>
    export default {
          data: function () {
        return {
            num: 0,
            op1: 0,
            op2: 0,
            operacion: 0
            }
        },
        methods: {
            capturar(input) {
               this.num = (this.num * 10) + input;
            },
            reset() {
                this.num = 0;
            },
            sumar(){
                this.op1 = this.num;
                this.num = 0;
                this.operacion = 1;                
            },
            restar(){
                this.op1 = this.num;
                this.num = 0;
                this.operacion = 2;      
            },
            multiplicar(){
                this.op1 = this.num;
                this.num = 0;
                this.operacion = 3; 
            },
            dividir(){
                this.op1 = this.num;
                this.num = 0;
                this.operacion = 4; 
            },
            igual(){
                this.op2 = this.num;
                switch (this.operacion) {
                    case 1:
                        this.num = this.op1 + this.op2;
                        break;
                    case 2:
                        this.num = this.op1 - this.op2;
                        break;
                    case 3:
                        this.num = this.op1 * this.op2;
                        break;
                    case 4:
                        this.num = this.op1 / this.op2;
                        break;
                    default:
                        break;
                }
            }
        }
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

.calc input {
    text-align: right;
    font-size: 2em;
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