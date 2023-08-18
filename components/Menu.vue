<template>
    <!-- <nav>
        <ul>
            <li>
                ESTATICO
                <NuxtLink to="/">Inicio</NuxtLink>
                <NuxtLink to="acerca">Acerca</NuxtLink>
                <NuxtLink to="contacto">Contacto</NuxtLink>

                 DINAMICO
                <NuxtLink :to="{ name:'index' }">Inicio</NuxtLink>
                <NuxtLink :to="{ name:'acerca' }">Acerca</NuxtLink>
                <NuxtLink :to="{ name:'contacto'}">Contacto</NuxtLink> 
            </li>
        </ul>
    </nav> -->
    <UVerticalNavigation :links="links" />
</template>

<script setup>
const links = [{
  label: 'Inicio',
  icon: 'i-heroicons-home',
  to: '/'
}, {
  label: 'Acerca de',
  icon: 'i-heroicons-chart-bar',
  to: '/acerca'
}, {
  label: 'Grilla',
  icon: 'i-heroicons-command-line',
  to: '/contacto'
}, {
  label: 'Productos',
  icon: 'i-heroicons-command-line',
  to: '/productos'
}]
</script>