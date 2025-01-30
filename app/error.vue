<script lang="ts" setup>
const error = useError();
const redirecting = ref(false);

const handleRedirect = () => {
    redirecting.value = true
    setTimeout(() => {
        clearError({ redirect: "/" });
    }, 3000);
}
</script>

<template>
    <Head>
        <Title>{{ redirecting ? "Redirecting..." : `Error ${error?.statusCode}` }}</Title>
    </Head>
    <div class="flex justify-center items-center h-screen">
        <div class="flex flex-col items-center gap-8">
            <div class="flex flex-col items-center">
                <h1 class="text-5xl font-bold">
                    {{ redirecting ? "Redirecting" : `Error ${error?.statusCode}` }}
                </h1>
                <p>{{ redirecting ? "Be Patient" : (error?.statusCode === 404 ? "Page Not Found"
                    : error?.statusCode === 500 ? "Internal Server Error" : "Error Occurred") }}</p>
            </div>
            <UButton label="Redirecting..." variant="ghost" loading v-if="redirecting" />
            <UButton label="Redirect" variant="soft" @click="handleRedirect" v-else />
        </div>
    </div>
</template>