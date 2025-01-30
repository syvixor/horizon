<script lang="ts" setup>
const isOpen = ref(false);
const links = [
    [
        {
            icon: "i-heroicons-squares-2x2",
            label: "Dashboard"
        },
        {
            icon: "i-heroicons-banknotes",
            label: "Transactions"
        },
        {
            icon: "i-heroicons-sparkles",
            label: "My Goals"
        },
        {
            icon: "i-heroicons-currency-dollar",
            label: "Investment"
        },
        {
            icon: "i-heroicons-document-text",
            label: "Bills & Payment"
        },
        {
            icon: "i-heroicons-chart-bar",
            label: "Analytics & Reports"
        }
    ],
    [
        {
            icon: "i-heroicons-question-mark-circle",
            label: "Help"
        },
        {
            icon: "i-heroicons-cube",
            label: "Integration"
        },
        {
            icon: "i-heroicons-cog-6-tooth",
            label: "Settings"
        }
    ]
];
</script>

<template>
    <div class="lg:hidden">
        <UButton icon="i-heroicons-bars-3" color="white" @click="isOpen = true" />
    </div>

    <USlideover v-model="isOpen">
        <div class="space-y-4 p-4">
            <div class="flex justify-between items-center">
                <p class="text-lg font-bold">Menu</p>
                <UButton icon="i-heroicons-x-mark" color="white" @click="isOpen = false" />
            </div>
            <UVerticalNavigation :links="links" />
        </div>
    </USlideover>
</template>