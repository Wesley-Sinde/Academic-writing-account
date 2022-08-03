<script setup>
import AppLayout from '@/Layouts/AppLayout.vue';
import Welcome from '@/Jetstream/Welcome.vue';
import Footerbt from '@/Jetstream/Footer.vue';
// import Sidebar from '@/Jetstream/Sidebar.vue';
</script>

<template>
    <AppLayout title="Dashboard">
        <template #header>
            <h2 class="text-xl font-semibold leading-tight text-gray-800 dark:text-gray-300">
                Dashboard
            </h2>
        </template>


        <div class="py-12">
            <div class="mx-auto max-w-7xl sm:px-6 lg:px-8">
                <div class="overflow-hidden bg-gray-200 shadow-xl dark:bg-gray-800 sm:rounded-lg">
                    <Welcome />
                </div>
            </div>
        </div>
        <Footerbt />
    </AppLayout>
</template>
