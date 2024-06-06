<template>
  <div id="app" class="p-4">
    <OrderList :pedidos="pedidos" />
  </div>
</template>

<script setup>
import { ref } from 'vue'
import OrderList from '../components/OrderList.vue'

const pedidos = ref([
  {
    id: 1,
    cliente: 'João Silva',
    produto: 'Cheeseburger',
    quantidade: 1,
    preco: 'R$ 25,00',
    data: '01/06/2024',
    status: 'Pendente',
    recebido: false
  },
  {
    id: 2,
    cliente: 'Maria Souza',
    produto: 'Bacon Burger',
    quantidade: 2,
    preco: 'R$ 50,00',
    data: '02/06/2024',
    status: 'Em Preparo',
    entregue: false,
    emPreparo: false
  },
  {
    id: 3,
    cliente: 'Maria Clara',
    produto: 'Bacon Burger',
    quantidade: 2,
    preco: 'R$ 50,00',
    data: '02/06/2024',
    status: 'Entregue',
    recebido: false
  },
  {
    id: 4,
    cliente: 'José Souza',
    produto: 'Bacon Burger',
    quantidade: 2,
    preco: 'R$ 50,00',
    data: '02/06/2024',
    status: 'Cancelado',
    recebido: false
  },
  {
    id: 5,
    cliente: 'José Souza',
    produto: 'Bacon Burger',
    quantidade: 2,
    preco: 'R$ 50,00',
    data: '02/06/2024',
    status: 'Cancelado',
    recebido: false
  },
  {
    id: 5,
    cliente: 'José Souza',
    produto: 'Bacon Burger',
    quantidade: 2,
    preco: 'R$ 50,00',
    data: '02/06/2024',
    status: 'Cancelado',
    recebido: false
  }
])
</script>

<style></style>
