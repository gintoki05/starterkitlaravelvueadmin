<script setup>
import Header from "@/Components/Layout/Header.vue";
import Sidebar from "@/Components/Layout/Sidebar.vue";
import { ref } from "vue";

const showingNavigationDropdown = ref(false);
</script>

<template>
    <div
        class="grid min-h-screen w-full md:grid-cols-[220px_1fr] lg:grid-cols-[280px_1fr]"
    >
        <Sidebar />
        <div class="flex flex-col">
            <Header />
            <main class="flex flex-1 flex-col gap-4 p-4 lg:gap-6 lg:p-6">
                <slot />
            </main>
        </div>
    </div>
</template>
