<script lang="ts" setup>
</script>

<template>
    <UCard class="p-2">
        <div class="flex justify-between items-center">
            <div class="flex items-center gap-4">
                <UAvatar src="https://avatars.githubusercontent.com/u/191499017?v=4" chip-color="green"
                    chip-position="bottom-right" size="md" />
                <div>
                    <p class="text-base font-semibold">Sckoorp</p>
                    <p class="text-sm font-normal">Hey There!</p>
                </div>
            </div>
            <div class="flex items-center gap-2">
                <UButton icon="i-heroicons-magnifying-glass" color="white" />
                <Theme />
                <Menu />
            </div>
        </div>
    </UCard>
</template>