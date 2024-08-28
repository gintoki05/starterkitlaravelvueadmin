<script setup>
import { defineProps, defineEmits, computed } from "vue";
import { Link, usePage } from "@inertiajs/vue3";
import * as Icons from "lucide-vue-next";

const props = defineProps({
    href: String,
    icon: String,
    label: String,
});

const page = usePage();

const isActive = computed(() => {
    return page.url.startsWith(props.href);
});
</script>

<template>
    <Link
        :href="href"
        @click="$emit('click')"
        :class="[
            'flex items-center gap-3 rounded-lg px-3 py-2 transition-all',
            isActive
                ? 'bg-muted text-primary'
                : 'text-muted-foreground hover:text-primary',
        ]"
    >
        <component :is="Icons[icon]" class="h-4 w-4" />
        <span>{{ label }}</span>
        <slot />
    </Link>
</template>
