<template>
  <div>
    <div class="texto">
      <label>Insertar texto:</label>
      <input type="text" v-model="value" />
    </div>
    <div v-if="cantidadCaracteres > 0">
      <p>Cantidad: {{ cantidadCaracteres }}</p>
      <p>{{ value | formatoCodificado }} (codificado)</p>
      <p>{{ value | formatoMayusc }} (mayúscula)</p>
      <p>{{ value | formatoMinusc }} (minúscula)</p>
      <p>{{ value | formatoMayuscMinusc }} (mayúscula/minúscula)</p>
      <p>{{ value | formatoMinuscMayusc }} (minúscula/mayúscula)</p>
    </div>
    <hr />
    <div>
      <p>respuestas: 1:b 2:b 3:c 4:b 5:b,c</p>
    </div>
  </div>
</template>

<script lang="js">

export default  {
  name: 'Codificacion',
  props: [],
  data () {
    return {
      value: "",
    }
  },
  computed: {
      cantidadCaracteres(){
          return this.value.length
      }
  },
   filters: {
     formatoCodificado: function(value){
        const vocales = {
          a: "u",
          e: "o",
          o: "e",
          u: "a"
      }

      return value.split("").map(element => vocales[element] ? vocales[element] : element).join("")
     },
     formatoMayusc: function(value){
      return value.toUpperCase()
     },
     formatoMinusc: function(value){
      return value.toLowerCase()
     },
     formatoMayuscMinusc: function(value){
      return value.split("").map((e, i) => (i + 1) % 2 == 0 ? e.toLowerCase() : e.toUpperCase()).join("")
     },
     formatoMinuscMayusc: function(value){
       return value.split("").map((e, i) => (i + 1) % 2 == 0 ? e.toUpperCase() : e.toLowerCase()).join("")
     },
   }
  }
</script>

<style scoped lang="css">
.texto {
  margin-bottom: 20px;
}
.texto label {
  padding-right: 10px;
}
</style>
