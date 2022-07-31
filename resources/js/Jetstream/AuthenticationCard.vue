<template>
    <div
        class="min-h-screen flex flex-col sm:justify-center items-center pt-6 sm:pt-0 bg-gray-100 dark:bg-gray-900 text-gray-600 dark:text-gray-300">
        <div>
            <slot name="logo" />
        </div>

        <div
            class="w-full sm:max-w-md mt-6 px-6 py-4 bg-gray-200 dark:bg-gray-800 border shadow-md overflow-hidden sm:rounded-lg text-gray-600 dark:text-gray-300">
            <slot />
        </div>
    </div>
</template>
