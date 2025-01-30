<script lang="ts" setup>
const transactions = [
    {
        type: "Receive",
        amount: "$800,00",
        status: "Waiting",
        method: "Bank Transfer"
    }, {
        type: "Sent",
        amount: "$1.100,00",
        status: "Cancelled",
        method: "Credit Card"
    }, {
        type: "Receive",
        amount: "$500,00",
        status: "Success",
        method: "Bank Transfer"
    }
];
</script>

<template>
    <div class="grid grid-cols-1 lg:grid-cols-[2fr,1fr] gap-4">
        <UCard>
            <div class="space-y-4 p-2">
                <div class="flex justify-between items-center">
                    <h4 class="text-lg font-bold">Recent Transactions</h4>
                </div>
                <UDivider />
                <UTable :rows="transactions" />
            </div>
        </UCard>
        <UCard>
            <div class="space-y-4 p-2">
                <div class="flex justify-between items-center">
                    <h4 class="text-lg font-bold">Pro Version</h4>
                </div>
                <UDivider />
                <UAlert icon="i-heroicons-star" color="primary" variant="soft" title="More with Premium!"
                    description="Our premium subscription elevates your experience and unlocks exclusive benefits to enhance it even further." />
                <div>
                    <p class="text-base font-normal">You'll Pay</p>
                    <div class="flex items-center">
                        <p class="text-lg font-bold">$19,99</p>
                        <p class="text-sm font-normal">/Month</p>
                    </div>
                </div>
                <UButton label="Learn More" color="sky"
                    class="transition-all hover:[filter:drop-shadow(0_0_0.5em_#428fb8aa)]" block />
            </div>
        </UCard>
    </div>
</template>