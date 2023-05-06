<script setup>


const produtos = [
    {
        id: 1,
        nome: 'Camiseta',
        preco: 49.90
    },
    {
        id: 2,
        nome: 'Calça',
        preco: 99.90
    },
    {
        id: 3,
        nome: 'Meia',
        preco: 9.90
    },
    {
        id: 4,
        nome: 'Sapato',
        preco: 199.90
    },
    {
        id: 5,
        nome: 'Boné',
        preco: 29.90
    },
    {
        id: 6,
        nome: 'Óculos',
        preco: 99.90
    },
    {
        id: 7,
        nome: 'Relógio',
        preco: 299.90
    },
    {
        id: 8,
        nome: 'Bermuda',
        preco: 79.90
    },
    {
        id: 9,
        nome: 'Cueca',
        preco: 19.90
    },
    {
        id: 10,
        nome: 'Meia',
        preco: 9.90
    }
]
  


</script>

<template>
<div class="container-fluid">
  <h1>loja CRF</h1>
   <img src="flamengo.webp" alt="fla">
</div>
<div>
  <ul>
<li v-for="items in produtos" :key="items.id" >{{ items.nome   }} - {{ items.preco }}
<button class="bot">adicionar ao carrinho</button>


 </li>

</ul></div>
   

</template>

<style scoped>

</style>
