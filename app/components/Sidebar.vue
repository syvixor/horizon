<script lang="ts" setup>
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
    <div class="fixed">
        <div class="hidden lg:flex flex-col justify-between w-60 h-screen p-4">
            <div class="space-y-4">
                <div class="flex justify-center items-center gap-4">
                    <img src="/logo.png" alt="horizon" class="w-10 h-10" />
                    <div class="-space-y-1">
                        <h3 class="text-xl font-bold">Horizon</h3>
                        <p class="text-xs font-normal">Your vision, streamlined.</p>
                    </div>
                </div>
                <UVerticalNavigation :links="links" />
            </div>
            <Upgrade />
        </div>
    </div>
</template>