<script setup lang="ts">
const colorMode = useColorMode();

const isLoading = ref(true);
onMounted(() => isLoading.value = false);

const onThemeSwitch = () => {
    colorMode.preference = colorMode.value === "dark" ? "light" : "dark"
}
</script>

<template>
    <ClientOnly v-if="!isLoading">
        <UButton :icon="colorMode.preference === 'dark' ? 'i-heroicons-moon' : 'i-heroicons-sun'" color="white"
            @click="onThemeSwitch" />
    </ClientOnly>
    <UButton color="white" variant="ghost" loading v-else />
</template>