<template>
    <div class="flex  items-center">
        <label class="relative flex items-center">
            <input type="text" placeholder="search" class=" pl-4 focus:outline-none focus:ring-2  placeholder-blue-900 text-lg form-input w-full h-10 rounded-lg">
            <svg class="h-5 absolute right-0 mr-2 text-gray-700 w-5" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" />
            </svg>
        </label>
    </div>
</template>

<script>
    export default {
        name: "Search"
    }
</script>

<style scoped>

</style>