<script setup>
  import { ref } from 'vue'


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
const carrinho = ref( [
    {
        id: 1,
        nome: 'Camiseta',
        preco: 49.90,
        quantidade: 0,
        valorTotal: 49.90
    },
    {
        id: 2,
        nome: 'Calça',
        preco: 99.90,
        quantidade: 0,
        valorTotal: 49.90
    },
    {
        id: 3,
        nome: 'Meia',
        preco: 9.90,
        quantidade: 0,
        valorTotal: 49.90
    },
    {
        id: 4,
        nome: 'Sapato',
        preco: 199.90,
        quantidade: 0,
        valorTotal: 49.90
    },
    {
        id: 5,
        nome: 'Boné',
        preco: 29.90,
        quantidade: 0,
        valorTotal: 49.90
    },
    {
        id: 6,
        nome: 'Óculos',
        preco: 99.90,
        quantidade: 0,
        valorTotal: 49.90
    },
    {
        id: 7,
        nome: 'Relógio',
        preco: 299.90,
        quantidade: 1,
        valorTotal: 49.90
    },
    {
        id: 8,
        nome: 'Bermuda',
        preco: 79.90,
        quantidade: 0,
        valorTotal: 49.90
    },
    {
        id: 9,
        nome: 'Cueca',
        preco: 19.90,
        quantidade: 0,
        valorTotal: 49.90
    },
    {
        id: 10,
        nome: 'Meia',
        preco: 9.90,
        quantidade: 0,
        valorTotal: 49.90
    }
])

const botao = ref(false)
function bot (){
    botao.value = true
}
function adicionar(produto){
    const index = carrinho.value.findIndex(item => item.id === produto.id)
    if (index > -1) {
        carrinho.value[index].quantidade++
    }     
}
function remover(produto){
 
    }





</script>

<template>
    <div class="container-fluid">
        <h1>loja CRF</h1>
        <img src="flamengo.webp" alt="fla">
    </div>
    <div>
        <ul>
            <li v-for="items in produtos" :key="items.id">{{ items.nome }} - {{ items.preco }}
                <button @click="adicionar(items)" class="bot">adicionar ao carrinho</button>
            </li>
        </ul>
    </div>
    <button @click="bot" type="button" class="btn btn-primary">Mostrar carrinho</button>

    <div v-if="botao == true">
        <ul>
            <li v-for="car in carrinho" :key="car.id">{{ car.nome }} - {{ car.preco }} - {{ car.quantidade }}
                <button @click="remover" class="bot">retirar do carrinho</button>
            </li>
        </ul>
    </div>
</template>

<style scoped>
.container-fluid {
    margin: 0 auto;
    text-align: center;
}
</style>
