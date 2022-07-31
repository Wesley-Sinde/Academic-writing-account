<script setup>
import { Head } from '@inertiajs/inertia-vue3';
import JetAuthenticationCardLogo from '@/Jetstream/AuthenticationCardLogo.vue';

defineProps({
    terms: String,
});
</script>

<template>

    <Head title="Terms of Service" />

    <div class="font-sans antialiased text-gray-900">
        <div class="pt-4 bg-gray-100">
            <div class="flex flex-col items-center min-h-screen pt-6 sm:pt-0">
                <div>
                    <JetAuthenticationCardLogo />
                </div>

                <div class="w-full p-6 mt-6 overflow-hidden prose bg-gray-200 shadow-md sm:max-w-2xl dark:bg-gray-800 sm:rounded-lg"
                    v-html="terms" />
            </div>
        </div>
    </div>
</template>
