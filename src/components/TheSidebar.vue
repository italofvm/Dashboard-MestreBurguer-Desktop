<template>
  <nav
    class="sm:w-[25%] lg:w-[260px] h-[95vh] p-3 bg-indigo-950 text-white rounded-tr-3xl flex flex-col items-left justify-between transition-all "
  >
    <ul>
      <RouterLink
        to="/"
        class="w-full py-3 px-1 hover:bg-indigo-900 ease-in-out duration-150 rounded flex items-center gap-2"
      >
        <span class="material-symbols-outlined text-2xl"> home </span>
        <span class="sm:hidden lg:flex">Geral</span>
      </RouterLink>

      <RouterLink
        to="/pedidos"
        class="w-full py-3 px-1 hover:bg-indigo-900 ease-in-out duration-150 rounded flex items-center gap-2"
      >
        <span class="material-symbols-outlined text-2xl"> assignment </span>
        <span class="sm:hidden lg:flex">Pedidos</span>
      </RouterLink>

      <RouterLink
        to="/clientes"
        class="w-full py-3 px-1 hover:bg-indigo-900 ease-in-out duration-150 rounded flex items-center gap-2"
      >
        <span class="material-symbols-outlined text-2xl"> groups </span>
        <span class="sm:hidden lg:flex">Clientes</span>
      </RouterLink>

      <RouterLink
        to="/funcionarios"
        class="w-full py-3 px-1 hover:bg-indigo-900 ease-in-out duration-150 rounded flex items-center gap-2"
      >
        <span class="material-symbols-outlined text-2xl"> assignment_ind </span>
        <span class="sm:hidden lg:flex"> Funcionários </span>
      </RouterLink>

      <RouterLink
        to="/promocao"
        class="w-full py-3 px-1 hover:bg-indigo-900 ease-in-out duration-150 rounded flex items-center gap-2"
      >
        <span class="material-symbols-outlined text-2xl"> sell </span>
        <span class="sm:hidden lg:flex">Promoções e Ofertas</span>
      </RouterLink>
    </ul>
    <RouterLink
      to="/settings"
      class="w-full py-3 sm:px-2 lg:px-1 hover:bg-indigo-900 ease-in-out duration-150 rounded flex items-center gap-2"
    >
      <span class="material-symbols-outlined text-2xl"> settings </span>
      <span class="sm:hidden lg:flex">Configurações</span>
    </RouterLink>
  </nav>

</template>

<script setup>
import { RouterLink } from 'vue-router'
</script>

<style scoped></style>
