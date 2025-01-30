<script lang="ts" setup>
const config = useAppConfig();
</script>

<template>
    <NuxtLoadingIndicator :color="config.color" />
    <Sidebar />
    <div class="space-y-4 lg:ml-60 p-4">
        <Header />
        <slot />
    </div>
    <UNotifications />
</template>