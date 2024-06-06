<template>
  <div class="container mx-auto p-6 h-[80%] border overflow-auto">
    <h1 class="text-2xl font-bold mb-4">Tabela de Pedidos</h1>
    <table class="min-w-full bg-white">
      <thead>
        <tr>
          <th class="py-2 px-4 bg-gray-200 border-b border-gray-300">ID</th>
          <th class="py-2 px-4 bg-gray-200 border-b border-gray-300">Cliente</th>
          <th class="py-2 px-4 bg-gray-200 border-b border-gray-300">Produto</th>
          <th class="py-2 px-4 bg-gray-200 border-b border-gray-300">Quantidade</th>
          <th class="py-2 px-4 bg-gray-200 border-b border-gray-300">Preço</th>
          <th class="py-2 px-4 bg-gray-200 border-b border-gray-300">Data</th>
          <th class="py-2 px-4 bg-gray-200 border-b border-gray-300">Status</th>
          <th class="py-2 px-4 bg-gray-200 border-b border-gray-300">Ações</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="pedido in pedidos" :key="pedido.id" :class="statusClass(pedido.status)">
          <td class="py-2 px-4 border-b border-gray-300">{{ pedido.id }}</td>
          <td class="py-2 px-4 border-b border-gray-300">{{ pedido.cliente }}</td>
          <td class="py-2 px-4 border-b border-gray-300">{{ pedido.produto }}</td>
          <td class="py-2 px-4 border-b border-gray-300">{{ pedido.quantidade }}</td>
          <td class="py-2 px-4 border-b border-gray-300">{{ pedido.preco }}</td>
          <td class="py-2 px-4 border-b border-gray-300">{{ pedido.data }}</td>
          <td class="py-2 px-4 border-b border-gray-300">{{ pedido.status }}</td>
          <td class="py-2 px-4 border-b border-gray-300">
            <select
              id="status"
              v-model="pedido.status"
              @change="handleStatusChange(pedido, $event.target.value)"
              class="block appearance-none w-full bg-white border border-gray-400 hover:border-gray-500 px-4 py-2 pr-8 rounded shadow leading-tight focus:outline-none focus:shadow-outline"
            >
              <option :class="statusClass('Pendente')" value="Pendente">Pendente</option>
              <option :class="statusClass('Em Preparo')" value="Em Preparo">Em Preparo</option>
              <option :class="statusClass('Cancelado')" value="Cancelado">Cancelado</option>
              <option :class="statusClass('Entregue')" value="Entregue">Entregue</option>
            </select>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script setup>
import { defineProps } from 'vue'

const props = defineProps({
  pedidos: {
    type: Array,
    required: true
  }
})


const statusClass = (status) => {
  switch (status) {
    case 'Pendente':
      return 'bg-yellow-100'
    case 'Em Preparo':
      return 'bg-blue-100'
    case 'Cancelado':
      return 'bg-red-100'
    case 'Entregue':
      return 'bg-green-100'
    default:
      return ''
  }
}

const handleStatusChange = (pedido, newStatus) => {
  pedido.status = newStatus
}

const { pedidos } = props
</script>

<style scoped></style>
