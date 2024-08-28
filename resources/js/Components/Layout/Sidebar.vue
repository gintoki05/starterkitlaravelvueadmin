<script setup>
import { Bell, Package } from "lucide-vue-next";
import NavigationLink from "./NavigationLink.vue";
import { Button } from "../ui/button";
import { Badge } from "../ui/badge";
</script>

<template>
    <div class="hidden border-r bg-muted/40 md:block">
        <div class="flex h-full max-h-screen flex-col gap-2">
            <div
                class="flex h-14 items-center border-b px-4 lg:h-[60px] lg:px-6"
            >
                <a href="/" class="flex items-center gap-2 font-semibold">
                    <Package class="h-6 w-6" />
                    <span>Acme Inc</span>
                </a>
                <Button variant="outline" size="icon" class="ml-auto h-8 w-8">
                    <Bell class="h-4 w-4" />
                    <span class="sr-only">Toggle notifications</span>
                </Button>
            </div>
            <div class="flex-1">
                <nav class="grid items-start px-2 text-sm font-medium lg:px-4">
                    <NavigationLink
                        href="/dashboard"
                        icon="Home"
                        label="Dashboard"
                    />
                    <NavigationLink href="#" icon="ShoppingCart" label="Orders">
                        <Badge
                            class="ml-auto flex h-6 w-6 shrink-0 items-center justify-center rounded-full"
                            >6</Badge
                        >
                    </NavigationLink>
                    <NavigationLink href="#" icon="Package" label="Products" />
                    <NavigationLink href="#" icon="Users" label="Customers" />
                    <NavigationLink
                        href="#"
                        icon="LineChart"
                        label="Analytics"
                    />
                </nav>
            </div>
        </div>
    </div>
</template>
