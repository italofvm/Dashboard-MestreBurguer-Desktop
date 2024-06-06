<!-- src/components/Settings.vue -->
<template>
  <div class="container mx-auto p-6 h-[80%] border overflow-auto">
    <h1 class="text-2xl font-bold mb-6">Configurações da Hamburgueria</h1>

    <!-- Informações do Restaurante -->
    <div class="bg-white p-6 rounded-lg shadow mb-6">
      <h2 class="text-xl font-semibold mb-4">Informações do Restaurante</h2>
      <form @submit.prevent="updateRestaurantInfo">
        <div class="mb-4">
          <label class="block text-gray-700">Nome do Restaurante</label>
          <input
            v-model="restaurant.name"
            type="text"
            class="mt-1 block w-full px-4 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring focus:ring-opacity-50"
          />
        </div>
        <div class="mb-4">
          <label class="block text-gray-700">Endereço</label>
          <input
            v-model="restaurant.address"
            type="text"
            class="mt-1 block w-full px-4 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring focus:ring-opacity-50"
          />
        </div>
        <div class="mb-4">
          <label class="block text-gray-700">Telefone</label>
          <input
            v-model="restaurant.phone"
            type="text"
            class="mt-1 block w-full px-4 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring focus:ring-opacity-50"
          />
        </div>
        <button
          type="submit"
          class="bg-blue-500 text-white px-4 py-2 rounded-md shadow-sm hover:bg-blue-700"
        >
          Salvar
        </button>
      </form>
    </div>

    <!-- Preferências de Notificação -->
    <div class="bg-white p-6 rounded-lg shadow mb-6">
      <h2 class="text-xl font-semibold mb-4">Preferências de Notificação</h2>
      <form @submit.prevent="updateNotifications">
        <div class="mb-4">
          <label class="block text-gray-700">Receber Notificações de Novos Pedidos por Email</label>
          <input v-model="notifications.email" type="checkbox" class="mt-1" />
        </div>
        <div class="mb-4">
          <label class="block text-gray-700">Receber Notificações de Novos Pedidos por SMS</label>
          <input v-model="notifications.sms" type="checkbox" class="mt-1" />
        </div>
        <button
          type="submit"
          class="bg-blue-500 text-white px-4 py-2 rounded-md shadow-sm hover:bg-blue-700"
        >
          Salvar
        </button>
      </form>
    </div>

    <!-- Configuração de Senha -->
    <div class="bg-white p-6 rounded-lg shadow">
      <h2 class="text-xl font-semibold mb-4">Configuração de Senha</h2>
      <form @submit.prevent="updatePassword">
        <div class="mb-4">
          <label class="block text-gray-700">Senha Atual</label>
          <input
            v-model="password.current"
            type="password"
            class="mt-1 block w-full px-4 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring focus:ring-opacity-50"
          />
        </div>
        <div class="mb-4">
          <label class="block text-gray-700">Nova Senha</label>
          <input
            v-model="password.new"
            type="password"
            class="mt-1 block w-full px-4 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring focus:ring-opacity-50"
          />
        </div>
        <div class="mb-4">
          <label class="block text-gray-700">Confirmar Nova Senha</label>
          <input
            v-model="password.confirm"
            type="password"
            class="mt-1 block w-full px-4 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring focus:ring-opacity-50"
          />
        </div>
        <button
          type="submit"
          class="bg-blue-500 text-white px-4 py-2 rounded-md shadow-sm hover:bg-blue-700"
        >
          Salvar
        </button>
      </form>
    </div>
  </div>
</template>

<script setup>
import { reactive } from 'vue'

const restaurant = reactive({
  name: '',
  address: '',
  phone: ''
})

const notifications = reactive({
  email: false,
  sms: false
})

const password = reactive({
  current: '',
  new: '',
  confirm: ''
})

const updateRestaurantInfo = () => {
  // Implementar a lógica para atualizar as informações do restaurante
  console.log('Informações do restaurante atualizadas:', restaurant)
}

const updateNotifications = () => {
  // Implementar a lógica para atualizar as preferências de notificação
  console.log('Notificações atualizadas:', notifications)
}

const updatePassword = () => {
  // Implementar a lógica para atualizar a senha
  console.log('Senha atualizada:', password)
}
</script>
