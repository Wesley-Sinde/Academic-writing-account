<script setup>
import { Head } from '@inertiajs/inertia-vue3';
import JetAuthenticationCardLogo from '@/Jetstream/AuthenticationCardLogo.vue';

defineProps({
    policy: String,
});
</script>

<template>

    <Head title="Privacy Policy" />

    <div class="font-sans antialiased text-gray-900 dark:text-gray-300">
        <div class="pt-4 bg-gray-200 dark:bg-gray-800">
            <div class="flex flex-col items-center min-h-screen pt-6 sm:pt-0">
                <div>
                    <JetAuthenticationCardLogo />
                </div>

                <div class="w-full p-6 mt-6 overflow-hidden prose bg-gray-200 shadow-md dark:bg-gray-800 sm:max-w-2xl sm:rounded-lg"
                    v-html="policy" />
            </div>
        </div>
    </div>
</template>
