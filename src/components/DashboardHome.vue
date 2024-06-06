<!-- src/components/Dashboard.vue -->
<template>
  <div class="container mx-auto p-6">
    <h1 class="text-3xl font-bold mb-4">Dashboard da Hamburgueria</h1>

    <!-- Resumo de Métricas Principais -->
    <div class="grid grid-cols-1 md:grid-cols-4 gap-6 mb-6">
      <div class="bg-white p-4 rounded-lg shadow">
        <h2 class="text-xl font-semibold">Total de Vendas</h2>
        <p class="text-2xl font-bold">R$ 75.000,00</p>
      </div>
      <div class="bg-white p-4 rounded-lg shadow">
        <h2 class="text-xl font-semibold">Pedidos</h2>
        <p class="text-2xl font-bold">2.350</p>
      </div>
      <div class="bg-white p-4 rounded-lg shadow">
        <h2 class="text-xl font-semibold">Clientes Satisfeitos</h2>
        <p class="text-2xl font-bold">1.890</p>
      </div>
      <div class="bg-white p-4 rounded-lg shadow">
        <h2 class="text-xl font-semibold">Itens Mais Vendidos</h2>
        <p class="text-2xl font-bold">Cheeseburger</p>
      </div>
    </div>

    <!-- Gráficos e Visualizações -->
    <div class="bg-white p-6 rounded-lg shadow mb-6">
      <h2 class="text-xl font-semibold mb-4">Gráfico de Vendas Mensais</h2>
      <!-- Coloque aqui o código ou componente para renderizar o gráfico -->
    </div>

    <!-- Últimos Pedidos -->
    <div class="bg-white p-6 rounded-lg shadow mb-6">
      <h2 class="text-xl font-semibold mb-4">Últimos Pedidos</h2>
      <ul>
        <li class="mb-2">Pedido #2345 - Cheeseburger, Batata Frita - 05/06/2024</li>
        <li class="mb-2">Pedido #2346 - Bacon Burger, Refrigerante - 05/06/2024</li>
        <!-- Adicione mais pedidos conforme necessário -->
      </ul>
    </div>

    <!-- Feedback dos Clientes -->
    <div class="bg-white p-6 rounded-lg shadow mb-6">
      <h2 class="text-xl font-semibold mb-4">Feedback dos Clientes</h2>
      <ul>
        <li class="mb-2">"Melhor hambúrguer que já comi!" - João Silva</li>
        <li class="mb-2">"Atendimento excelente!" - Maria Souza</li>
        <!-- Adicione mais feedbacks conforme necessário -->
      </ul>
    </div>

    <!-- Alertas e Notificações -->
    <div class="bg-red-100 p-4 rounded-lg shadow mb-6">
      <h2 class="text-xl font-semibold text-red-600">Alertas</h2>
      <p class="text-red-600">Nenhum alerta crítico no momento.</p>
    </div>
  </div>
</template>

<script setup></script>
