<template>
    <div>
        <header>
            Sitio de prueba para NuxtLabs
        </header>
    </div>
    <ClientOnly>
        <UButton
        :icon="isDark ? 'i-heroicons-moon-20-solid' : 'i-heroicons-sun-20-solid'"
        color="gray"
        variant="ghost"
        aria-label="Theme"
        @click="isDark = !isDark"
        />

        <template #fallback>
        <div class="w-8 h-8" />
        </template>
    </ClientOnly>

    <div class="grid md:grid-cols-5 gap-4">
        <Menu class="col-span-1">
        </Menu>
        <main class="col-span-4">
            <slot>

            </slot>
        </main>
    </div>

    <footer>&copy; Ortega Diego -  {{ añoActual }}</footer>
</template>

<script setup>
    const añoActual = new Date().getUTCFullYear();
    const colorMode = useColorMode()

    const isDark = computed({
    get () {
        return colorMode.value === 'dark'
    },
    set () {
        colorMode.preference = colorMode.value === 'dark' ? 'light' : 'dark'
    }
    })
</script>
