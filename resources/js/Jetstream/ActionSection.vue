<script setup>
import JetSectionTitle from './SectionTitle.vue';
</script>

<template>
    <div class="md:grid md:grid-cols-3 md:gap-6">
        <JetSectionTitle>
            <template #title>
                <slot name="title" />
            </template>
            <template #description>
                <slot name="description" />
            </template>
        </JetSectionTitle>

        <div class="mt-5 md:mt-0 md:col-span-2">
            <div class="px-4 py-5 bg-gray-200 shadow sm:p-6 dark:bg-gray-800 sm:rounded-lg">
                <slot name="content" />
            </div>
        </div>
    </div>
</template>
