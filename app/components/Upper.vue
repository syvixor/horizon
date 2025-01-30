<script lang="ts" setup>
const overview = [
    {
        name: "Transaction",
        result: 40
    },
    {
        name: "Income",
        result: 24
    },
    {
        name: "Outcome",
        result: 16
    }
];

function getTodayDate() {
    return new Date().toLocaleDateString("en-US", { month: "long", year: "numeric" });
}
</script>

<template>
    <div class="grid grid-cols-1 lg:grid-cols-3 gap-4">
        <UCard>
            <div class="space-y-4 p-2">
                <div class="flex justify-between items-center">
                    <h4 class="text-lg font-bold">Overview</h4>
                    <p class="text-sm font-normal">{{ getTodayDate() }}</p>
                </div>
                <UDivider />
                <div class="grid grid-cols-3 items-center gap-2">
                    <div class="flex flex-col items-center" v-for="o in overview">
                        <h4 class="text-lg font-bold">{{ o.result }}</h4>
                        <p class="text-base font-normal">{{ o.name }}</p>
                    </div>
                </div>
            </div>
        </UCard>
        <UCard>
            <div class="space-y-4 p-2">
                <div class="flex justify-between items-center">
                    <h4 class="text-lg font-bold">Balance</h4>
                    <p class="text-sm font-normal">$ US Dollar</p>
                </div>
                <UDivider />
                <div class="flex justify-between items-center">
                    <div>
                        <p class="text-base font-normal">Balance</p>
                        <h4 class="text-lg font-bold">$20.088,36</h4>
                    </div>
                    <UButton icon="i-heroicons-credit-card" variant="ghost" size="xl" />
                </div>
            </div>
        </UCard>
        <UCard>
            <div class="space-y-4 p-2">
                <div class="flex justify-between items-center">
                    <h4 class="text-lg font-bold">Quick Action</h4>
                </div>
                <UDivider />
                <div class="space-y-1">
                    <UButton icon="i-heroicons-arrow-left-20-solid" color="sky" size="sm" variant="soft" block>
                        Send Money</UButton>
                    <UButton icon="i-heroicons-arrow-right-20-solid" color="orange" variant="soft" size="sm" block>
                        Request Money</UButton>
                </div>
            </div>
        </UCard>
    </div>
</template>