<template>
    <div class="home">
        Ingrese primer numero: <input type="number" v-model="Numero1" /><br />
        Ingrese segundo numero <input type="number" v-model="Numero2" /><br />

        <button type="button" v-on:click="Sumar">
            Sumar
        </button><br />

        <button type="button" v-on:click="Resta">
            Resta
        </button><br />

        <button type="button" v-on:click="Multiplicacion">
            Multiplicacion
        </button><br />

        <button type="button" v-on:click="Division">
            Division
        </button><br />

        <span>
            Resultado: {{Resultado}}
        </span>


    </div>
</template>

<script>
    export default {
        data() {
            return {
                
                Numero1: '',
                Numero2: '',
                Resultado: 0,

            }
        },
        methods:{
            Sumar() {
                this.Resultado = parseFloat(this.Numero1) + parseFloat(this.Numero2);
                                
            },

            Resta() {
                this.Resultado = (+this.Numero1) - (+this.Numero2);
            },

            Multiplicacion() {
                this.Resultado = (+this.Numero1) * (+this.Numero2);
            },

            Division() {
                if (this.Numero2 == 0) {

                    alert('No se puede dividir entre 0');
                }
                else {
                    this.Resultado = this.Numero1 / this.Numero2;

                }
                 
            }


        }
    };
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    



</style>
