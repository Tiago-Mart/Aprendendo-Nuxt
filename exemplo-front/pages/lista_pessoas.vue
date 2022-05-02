<template>
  <div>
      <h1> {{titulo}}</h1>
      <ul>
          <!-- Busca por items em pessoas e usa os dados-->
          <li :key="item.id" v-for="item in pessoas">
              <!-- Saída: Nome - Idade: X anos-->
              {{item.nome}} - Idade: {{item.idade}} anos
          </li>
          <button @click="digaOla">  Clique aqui </button>
      </ul>
  </div>
</template>

<script>
export default {
    data: function(){
        return{
            titulo: "Lista de Pessoas e Idades",
            pessoas: [
                { id: 1, nome: "Marcio", idade: "33"},
                { id: 2, nome: "Diego", idade: "44"},
                { id: 3, nome: "João", idade: "50"},
                { id: 4, nome: "Carla", idade: "24"},
                { id: 5, nome: "José", idade: "28"},
                { id: 6, nome: "Maria", idade: "22"},
                { id: 7, nome: "Eduardo", idade: "29"},
                { id: 8, nome: "Clara", idade: "26"},
                { id: 9, nome: "Olivia", idade: "23"},
            ]
        }
    },
    methods:{
        digaOla: function(){
            alert("Isso é um alerta!");
        }
    }
}
</script>

<style>

</style>